SET(${PROJECT_NAME}_PYTHON_TESTS
  trivial
  geometry
  scenario
  serialization_examples
  )

FOREACH(TEST ${${PROJECT_NAME}_PYTHON_TESTS})
  ADD_PYTHON_UNIT_TEST("py-${TEST}" "unittest/python/${TEST}.py" "bindings/python")
ENDFOREACH(TEST ${${PROJECT_NAME}_PYTHON_TESTS})
