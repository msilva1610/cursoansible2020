# Treinamento ansible

## Erros encontrados

### Erro no vagrant up
msg
```
Error: dyld: Library not loaded: /usr/local/opt/openssl/lib/libcrypto.1.0.0.dylib
  Referenced from: /usr/local/bin/ssh
  Reason: image not found
rsync: connection unexpectedly closed (0 bytes received so far) [sender]
rsync error: error in rsync protocol data stream (code 12) at /BuildRoot/Library/Caches/com.apple.xbs/Sources/rsync/rsync-52/rsync/io.c(453) [sender=2.6.9]
```

### Tentativa 3 - Funcionou!!! 14/04/2020

Removi a instalação da versão atual do openssh

```
brew uninstall --ignore-dependencies openssl
```

E, instalei a versão requerida com o comando

```
brew install https://github.com/tebelorg/Tump/releases/download/v1.0.0/openssl.rb
```