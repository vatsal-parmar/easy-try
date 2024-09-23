# easy-try

A simple utility function for easier error handling in asynchronous JavaScript operations.

## Installation

```bash
npm install easy-try
```

## Usage

```javascript
const easyTry = require("easy-try");

// Example usage
async function fetchData() {
  const [data, error] = await easyTry(fetch("https://api.example.com/data"));

  if (error) {
    console.error("Error fetching data:", error);
    return;
  }

  console.log("Data fetched successfully:", data);
}
```

## API

### `easyTry<T, E = Error>(promise: Promise<T>): Promise<[T, null] | [null, E]>`

Wraps a promise and returns a tuple with either the resolved value and null, or null and the caught error.

#### Parameters

- `promise`: The promise to be handled.

#### Returns

- A promise that resolves to a tuple:
  - If the input promise resolves: `[resolvedValue, null]`
  - If the input promise rejects: `[null, error]`

## TypeScript Support

This utility is written in TypeScript and provides full type support.

## License

MIT

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check issues page if you want to contribute.

## Author

Vatsal Parmar

## Support

If you have any questions or need help using this package, please open an issue in the GitHub repository.
