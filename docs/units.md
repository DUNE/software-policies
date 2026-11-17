# Units

<span class="status ratify">For ratification</span> · Version 2 · Owners: Brett Viren, Gavin S. Davies

**Authoritative text:** *A Standard System of Units for DUNE in the Phlex Era*, version 2, [DocDB 38407](https://docs.dunescience.org/cgi-bin/sso/ShowDocument?docid=38407). The technical case and the three software packages are Brett Viren's ([20 August 2026 talk](https://indico.fnal.gov/event/75778/contributions/347641/attachments/200812/280154/hep-units.pdf)).

Applies to DUNE code and configuration written for Phlex. Existing art and LArSoft code that is not being migrated is out of scope.

## The decisions

| | Decision |
|---|---|
| D1 | DUNE adopts the CLHEP system of units. The unit constants are `double`; a quantity may be stored as `float` by deliberate, documented choice. |
| D2 | Two coding rules: multiply by a unit when a number a person wrote enters the code; divide by a unit when a number leaves for a person. |
| D3 | All configuration is in the system of units, in every language Phlex accepts. Jsonnet uses unit constants; JSON, YAML and FHiCL use unit strings such as `"100 * MeV"`. |
| D4 | `hep-config`, built on `hep-units` and `boost-config`, is the supported implementation. |
| D5 | Code with other units, LArSoft first of all, sits behind a units firewall, crossed only through shared, tested conversion helpers. |
| D6 | New DUNE data products are converted at the firewall. Wrapped LArSoft products are allowed during the migration; bare LArSoft types are not allowed in new code. |
| D7 | The three generic packages move from a personal account to a shared organization. DUNE's own units code lives in `dune-core` and `dune-obj`. |
| D8 | The rules live on this site, with DUNE's other software policies. A deviation is a bug; code review and automated checks look for it. |

## The two rules

```cpp
namespace units = hep::units;

// In: a number a person wrote. Multiply by its unit.
double threshold = 5 * units::keV;
double drift     = 1.6 * units::mm / units::us;

// Out: a number leaving for a person. Divide by the unit you want.
std::cout << baseline / units::km << " km\n";
```

Between those two points a unit constant never appears. For a physical constant, use the one `hep-units` provides (`c_light`, `hbarc`, the particle masses); for any other value, name its source in a comment beside the unit.

## Code review checklist

- New dimensionful literals carry a unit.
- Configuration goes through a config struct and `hep-config`.
- Values from LArSoft go through a firewall helper, never an inline `x * units::cm`.
- A quantity stored as `float` says why.

## Phase 2: units as types

Compile-time checking with typed quantities (for example mp-units) is proposed as a separate second phase, starting after ratification with a list of requirements. Typed quantities may already be used inside an algorithm, provided its configuration and its data products follow D1 to D8.

## History

| Version | Date | Change |
|---|---|---|
| 1 | 12 Oct 2026 | Proposal for comment, presented at the CSC General Meeting. Comments to 2 Nov 2026. |
| 2 | 17 Nov 2026 | Revised after comments, for ratification at CRAB on 19 Nov 2026. Phase 2 added; every comment answered in Appendix B. |
