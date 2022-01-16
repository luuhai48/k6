# K6.io - API load testing tool

---

## Installation

### MacOS

Using [Homebrew](https://brew.sh/):

```bash
brew install k6
```

### For other OS

Follow instruction on [k6.io](https://k6.io/docs/getting-started/installation/)

---

## Example

#### Run with 1 vu (Virtual user)

```bash
k6 run example.js
```

#### Run 10 vu (Virtual users) in 30s

```bash
k6 run --vus 10 --duration 30s example.js
```

---

## Results output

#### InfluxDB + Grafana

Before running the test, start the docker containers:

```bash
docker-compose up -d

# Or using Make
make up
```

Then

```bash
k6 run --out influxdb=http://localhost:8086/k6 example.js
```
