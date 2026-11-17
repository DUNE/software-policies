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

## Copyright and Licensing
Copyright © 2026 FERMI NATIONAL ACCELERATOR LABORATORY for the benefit of the DUNE Collaboration.

This repository, and all software contained within, is licensed under
the Apache License, Version 2.0 (the "License"); you may not use this
file except in compliance with the License. You may obtain a copy of
the License at

    http://www.apache.org/licenses/LICENSE-2.0

Copyright is granted to FERMI NATIONAL ACCELERATOR LABORATORY on behalf
of the Deep Underground Neutrino Experiment (DUNE). Unless required by
applicable law or agreed to in writing, software distributed under the
License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for
the specific language governing permissions and limitations under the
License.
