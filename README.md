# Unhandled FormatException in JSON Decoding

This repository demonstrates a common error in Dart when handling HTTP responses and JSON decoding.  The code attempts to parse a JSON response but fails to handle the `FormatException` that occurs when the response body is not valid JSON.  The solution provides improved error handling to gracefully manage this scenario.

## Bug

The `bug.dart` file contains the code with the error.  The `jsonDecode` function is called directly without checking if the response body is valid JSON. This leads to a crash if the server returns an unexpected response.

## Solution

The `bugSolution.dart` file provides a solution by adding proper error handling.  It uses a `try-catch` block to handle the potential `FormatException` and logs an informative error message instead of crashing the application.