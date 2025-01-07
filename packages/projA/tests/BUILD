python_test_utils(
    name="test_utils",
)

python_tests(name="projA_tests",
    dependencies=["packages/projA/src/projA:projA"],
    entry_point_dependencies={
        "packages/projA:projA_package": ["test"],
    }
)