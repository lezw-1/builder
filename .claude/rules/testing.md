# Testing

## Test Strategy
- Follow the **testing pyramid**: many unit tests, fewer integration tests, minimal end-to-end tests.  
- Test **behavior, not implementation** — tests should survive internal refactors.  
- Write tests **before fixing bugs** to prove the bug exists and that the fix resolves it.  

## Unit Tests
- Each test should verify **one behavior**.  
- Tests must be **fast, isolated, and deterministic**.  

## Integration Tests
- Test the **interaction between real components** (e.g., service + database).  
- Use **isolated environments** (test databases, containers).  
- **Clean up test data** after each test run.

## Test Quality
- Tests that **never fail are not valuable**.  
- Maintain **test coverage as a floor, not a ceiling**.  
