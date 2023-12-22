# otel-go-contrib

## Usage

### Gin HTTP Metrics using Opentelemetry

```golang
import "github.com/userwerk/otel-go-contrib/otelginmetrics"
router := gin.Default()
router.Use(otelginmetrics.Middleware("hello world"))
```

### HTTP Client Metrics using Opentelemetry

```golang
import "github.com/userwerk/otel-go-contrib/otelhttpmetrics"
transport := otelhttpmetrics.NewTransport(http.DefaultTransport)
client := http.DefaultClient
client.Transport = transport
```
