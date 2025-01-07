python_source(
    name="setup",
    source="setup.py",
    dependencies=[":version"],
)

resource(name="pyproject", source="pyproject.toml")
resource(name="setup_cfg", source="setup.cfg")


python_distribution(
    name="projB_package",
    dependencies=[
        ":pyproject",
        ":setup",
        ":setup_cfg",
        "packages/projB/src/projB:projB",
    ],
    provides=python_artifact(
        name="projB",
    ),
    entry_points = {
        "test":{"projB": "projB.conftest.run"},
    },
    generate_setup = False
)