OpenSSL RSA Playground
======================

Hi! This is a very simple repo with commands for working
with RSA keys in a very easy way.

```bash
# Create the key
ssh-keygen -t rsa -b 2048 -f private.key

# Remove the SSH public key
rm -f private.key.pub

# Create the true public key
openssl rsa -in private.key -pubout -out public.key

# Create a message
vim mensagem

# Protect the message
openssl rsautl -encrypt -pubin -inkey public.key -in mensagem -out mensagem_protegida

# Decrypt
openssl rsautl -decrypt -inkey private.key -in mensagem_protegida -out mensagem_decifrada

```

That is it! I will add more encryption forms later. Bye!

