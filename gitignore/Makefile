.PHONY: setup run test

# Installs pip-tools if missing, locks dependencies, and installs from the lock file
setup:
	python -m pip install --upgrade pip pip-tools
	pip-compile requirements.in -o requirements.lock
	pip install -r requirements.lock

run:
	python src/pipeline.py

test:
	python -c "import duckdb, polars, pandera; print('Environment verified!')"