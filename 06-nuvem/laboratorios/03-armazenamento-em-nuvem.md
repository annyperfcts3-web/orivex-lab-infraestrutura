## 5. Validação de controle de acesso

Após o upload do arquivo `orivex-lab.txt`, foi realizado um teste
de acesso utilizando a URL do objeto no navegador.

**Resultado obtido:**
- Resposta: `AccessDenied`
- Acesso anônimo: negado
- Arquivo armazenado no bucket: `orivex-lab-storage-2026-1313313`
- Região: `us-east-2` (Ohio)

**Conclusão:**

O teste demonstrou que o objeto não está disponível para acesso
anônimo pela URL direta, conforme a configuração de bloqueio
de acesso público do bucket.

**Conceitos praticados:** Amazon S3, armazenamento de objetos,
bloqueio de acesso público e controle de permissões.