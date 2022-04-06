Responsible for sending an individual event to the Redis queue.

This expects a query string with the follow query params:

- ulid: The ULID for the session
- food: The name of the food
- correct: The string value `t` (or `true`) for correct. 

It then transforms this data into the following JSON data that is sent to Redis:

```json
{
    "ulid": "ULID",
    "food": "food name",
    "correct": true
}
```

## Building

Run `make build` in this directory to build.

To serve, use the `spin.toml` file in the parent directory.