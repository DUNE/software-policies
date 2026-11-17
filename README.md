# DUNE Software Policies

Every DUNE software policy, its status, its owner and its text, published at
<https://dune.github.io/software-policies/>.

Each policy is a Markdown page under `docs/`. A change to a policy is a pull
request, reviewed like code. Substantive changes follow the comment and
ratification process in `docs/process.md`.

## Build

The site uses [Zensical](https://zensical.org/). The virtual environment lives
outside the repository, in `~/venvs/dune-software-policies`.

```sh
make install       # uv sync
make serve         # local preview
make build         # build into site/
make check-public  # no local paths in the tree or history
```
