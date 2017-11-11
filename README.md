# faas-gobuster

A basic PoC of using [@OJ's](https://github.com/OJ) [gobuster](https://github.com/OJ/gobuster) with [OpenFaaS](https://www.openfaas.com/) by [Glenn 'devalias' Grant](http://devalias.net/) ([@_devalias](https://twitter.com/_devalias))

## Usage

```
faas-cli deploy -f stack.yml
echo "-w /words/quicktestwords.txt -u http://example.com" | faas-cli invoke gobuster
```

## See Also

* https://github.com/0xdevalias/docker-gobuster ([DockerHub](https://hub.docker.com/r/devalias/gobuster/))
