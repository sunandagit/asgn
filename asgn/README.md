# Service 

This Python script implements a web service using Flask framework with two endpoints:

1. **Version 1 Endpoint:** `/reply/<string:code>`
   - Accepts a string input and returns it in a JSON object.
   
2. **Version 2 Endpoint:** `/v2/reply/<int:id>-<string:code>`
   - Accepts an integer as the rule and a string input.
   - Performs operations on the string input based on the digits of the rule:
     - If the rule has two digits:
       - If the first digit is 1, the string is reversed.
       - If the first digit is 2, the string is hashed using MD5.
       - If the first digit is neither 1 nor 2, returns an error message.
     - If the rule does not have two digits, returns an error message.
   - Returns the modified string or an error message in a JSON object.


# Test App Module 

This module contains unit tests for the service functionality using the unittest framework in Python.

Test Cases

1. **test_v1_success**: Tests a successful response from the '/reply' endpoint with a simple string input.

2. **test_v2_success_1**
3. **test_v2_success_2**
4. **test_v2_success_3**
5. **test_v2_success_4**

These tests a successful response from the '/v2/reply' endpoint with a specific string input and different combitation of the rule.

6. **test_v2_invalid_input_failure_1**: 
7. **test_v2_invalid_input_failure_2**: 
8. **test_v2_invalid_input_failure_3**:

These tests a failure response from the '/v2/reply' endpoint with an invalid input.








