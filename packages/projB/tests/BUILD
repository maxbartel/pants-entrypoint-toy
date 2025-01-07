python_test_utils(
    name="test_utils",
)

python_tests(name="projB_tests",
    dependencies=["packages/projB/src/projB:projB"],
    entry_point_dependencies={
        "packages/projB:projB_package": ["test"],
    }
)