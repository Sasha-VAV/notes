### Polars
Is a fast analog for pandas

[Documentation](https://docs.pola.rs/user-guide/getting-started/)

Installation
```shell
uv pip install polars   
```

```shell
df = dataset.dataset
    with pl.SQLContext(register_globals=True, eager=True) as context:
        other = context.execute("""
        SELECT *
        FROM df
        WHERE a > 6
        LIMIT 10;
        """)
        print(other)
```