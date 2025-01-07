python_source(
    name="setup",
    source="setup.py",
    dependencies=[":version"],
)

resource(name="pyproject", source="pyproject.toml")
resource(name="setup_cfg", source="setup.cfg")


python_distribution(
    name="projA_package",
    dependencies=[
        ":pyproject",
        ":setup",
        ":setup_cfg",
        "packages/projA/src/projA:projA",
    ],
    provides=python_artifact(
        name="projA",
    ),
    entry_points = {
        "test":{"projA": "src.projA.conftest.run"},
    },
    generate_setup = False
)