# ctf-robot-signin

An example challenge for Web category in CTF competitions.

## Run and Build

Use cargo to run or build.

```bash
cargo run
```

```bash
cargo build --release --bin web_server
```

You can configure the following environment variables to change the behavior of the server:

| Variable Name | Default Value   | Description                    |
|---------------|-----------------|--------------------------------|
| `BIND_ADDR`   | `0.0.0.0:80`    | The address that server binds. |
| `STATIC_PATH` | `/var/www/html` | The path to the static files.  |
| `FLAG`        | N/A             | FLAG content to the challenge. |

## Docker

[Dockerfile](Dockerfile) is provided at the root of the project. You can build the image with the following command:

```bash
docker build -t ctf-robot-signin:latest .
```

Then run the container with:

```bash
docker run -d -e 'FLAG=flag{example_real_flag}' -p 8000:80 ctf-robot-signin:latest
```

Or you can use the [docker-compose.yml](docker-compose.yml) file to run the container with:

```bash
docker-compose up -d
```

Then visit `http://localhost:8000` to see the challenge page.

## License

CopyRight (c) Cnily03. All rights reserved.

Licensed under the [MIT](LICENSE) License.
