# 📓 Como Configurar o Arquivo Hosts no Linux e macOS  

Esse tutorial é para você que é aluno ou aluna do Cypress Skills, testando a RockShaver localmente e precisa mapear nomes de domínio personalizados para `127.0.0.1` no arquivo **hosts**. 

```shell
127.0.0.1 rockshaver-mob
127.0.0.1 rockshaver-api
127.0.0.1 rockshaver-db
127.0.0.1 mongoexpress
```

---

## 🐧 Configurando no Linux  

### 1. Abra o terminal  

### 2. Faça um backup do arquivo hosts (opcional)  

Sempre é bom garantir que o arquivo original esteja seguro. Para isso, execute:  

```bash
sudo cp /etc/hosts /etc/hosts.bak
```

### 3. Edite o arquivo hosts

Abra o arquivo com permissões de superusuário usando o editor de sua preferência, como o `nano`:

```bash
sudo nano /etc/hosts
```

### 4. Adicione os domínios personalizados

Role até o final do arquivo e insira as seguintes linhas:

```bash
127.0.0.1    rockshaver-web  
127.0.0.1    rockshaver-mob  
127.0.0.1    rockshaver-api  
127.0.0.1    rockshaver-db  
127.0.0.1    mongoexpress
```

### 5. Salve e saia

- Pressione `Ctrl + O` para salvar.
- Pressione `Enter` para confirmar.
- Pressione `Ctrl + X` para sair do editor.

### 6. Verifique se as mudanças funcionaram (opcional)

Execute o comando `ping` para testar o mapeamento:

```bash
ping rockshaver-web
```

------

## 🍎 Configurando no macOS

### 1. Abra o terminal

No macOS, pressione `Command + Space`, digite "Terminal" e pressione `Enter`.

### 2. Faça um backup do arquivo hosts (opcional)

Para evitar qualquer problema, crie um backup:

```bash
sudo cp /etc/hosts /etc/hosts.bak
```

### 3. Edite o arquivo hosts

Use o comando abaixo para abrir o arquivo hosts no editor `nano`:

```bash
sudo nano /etc/hosts
```

### 4. Adicione os domínios personalizados

Adicione as linhas abaixo ao final do arquivo:

```bash
127.0.0.1    rockshaver-web  
127.0.0.1    rockshaver-mob  
127.0.0.1    rockshaver-api  
127.0.0.1    rockshaver-db  
127.0.0.1    mongoexpress
```

### 5. Salve e saia

- Pressione `Ctrl + O` para salvar.
- Pressione `Enter` para confirmar.
- Pressione `Ctrl + X` para sair do editor.

### 6. Limpe o cache de DNS

Para aplicar as mudanças imediatamente, execute:

```bash
sudo dscacheutil -flushcache
```

### 7. Verifique se as mudanças funcionaram (opcional)

Execute o comando `ping` para testar:

```bash
ping rockshaver-web
```

## 🔍 Dicas Finais

- **Localização do arquivo hosts**: O caminho do arquivo é sempre `/etc/hosts`, tanto no Linux quanto no macOS.
- **Permissões administrativas**: Você precisará de privilégios de superusuário para editar o arquivo.
- **Cache de DNS**: No macOS, lembre-se de limpar o cache de DNS para aplicar as alterações imediatamente.
