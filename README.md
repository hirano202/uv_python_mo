# init

uv init example
cd example
tree
.
├── README.md
├── hello.py
└── pyproject.toml

# uv lock のみ作る場合

uv.lock

# add package で自動的に uv.lock が作られる

uv add ruff
tree
.
├── README.md
├── hello.py
├── pyproject.toml # content add
└── uv.lock # add
uv remove ruff

# add pacakge dev

uv add --dev ruff
uv remove --dev ruff

uv tool install ruff
uv tool run ruff check hello.py

> All checks passed!

# venv を作る

uv venv --python 3.12
source .venv/bin/activate
which python # ここで interpreter を設定
uv sync
uv pip list

# other

deactivate
mypy .
