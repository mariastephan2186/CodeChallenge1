# Test Coverage Documentation

## Overview
This project uses Playwright for end-to-end testing of cryptocurrency trading operations. The tests cover the main user flows for buying, selling, and swapping cryptocurrencies, including MetaMask wallet interactions.

## Test Setup
- Tests automatically verify server availability before execution
- Base URL is configurable via `APP_URL` environment variable (defaults to `http://localhost:3000`)
- Each test includes automatic wallet connection in the setup phase

## Covered Flows

### Pre-test Checks
- ✅ Server availability verification
- ✅ Automatic retry logic for page navigation
- ✅ Wallet connection verification

### Buy Cryptocurrency Flow
- ✅ Navigation to buy section
- ✅ Input of purchase amount
- ✅ Payment method selection
- ✅ Transaction confirmation
- ✅ MetaMask interaction
- ✅ Success verification

### Sell Cryptocurrency Flow
- ✅ Navigation to sell section
- ✅ Input of sell amount
- ✅ Receiving method selection
- ✅ Transaction confirmation
- ✅ MetaMask interaction
- ✅ Success verification

### Token Swap Flow
- ✅ Navigation to swap interface
- ✅ Token selection (ETH → USDT)
- ✅ Swap amount specification
- ✅ Estimated output verification
- ✅ Transaction confirmation
- ✅ MetaMask interaction
- ✅ Success verification

## Test Data
- Buy operation tests with 0.1 token amount
- Sell operation tests with 0.05 token amount
- Swap operation tests with 0.1 ETH to USDT

## Important Notes
1. Tests use data-testid attributes for reliable element selection
2. Each major operation is broken down into logical steps using `test.step()`
3. MetaMask interactions are handled in separate contexts
4. Network idle waiting is implemented for reliable page loading
5. Error handling includes proper cleanup of resources

## Running the Tests
Ensure your development server is running before executing tests. The test suite will automatically check for server availability and provide helpful error messages if the server is not running.
