# Carsai LMS - Sistema de Gestão de Aprendizagem

Este é um sistema completo de gestão de aprendizagem (LMS) desenvolvido para a Carsai Mozambique.

## Características

- **Área Pública**: Página inicial, listagem de cursos, páginas institucionais
- **Área do Estudante**: Dashboard, gestão de cursos, perfil
- **Área do Formador**: Gestão de cursos, estudantes, conteúdo
- **Área Administrativa**: Gestão completa do sistema
- **Sistema de Pagamentos**: Integração com M-Pesa, e-Mola, mKesh e PayPal
- **Design Responsivo**: Compatível com desktop, tablet e mobile

## Requisitos do Sistema

- PHP 7.4 ou superior
- MySQL 5.7 ou superior
- Apache ou Nginx
- SSL (recomendado)

## Instalação

1. **Fazer upload dos arquivos** para seu servidor web
2. **Configurar permissões**: 
   ```bash
   chmod 755 ./
   chmod 755 uploads/
   chmod 644 configs/config.php
   ```
3. **Criar banco de dados MySQL** para o sistema
4. **Acessar o instalador**: Abra seu navegador e vá para `seu-dominio.com/instalacao.php`
5. **Seguir as instruções** do instalador para configurar o sistema
6. **Após instalação**, remover o arquivo `instalacao.php` por segurança

## Estrutura de Diretórios

```
carsai-lms/
├── admin/                 # Área administrativa
│   ├── includes/         # Arquivos de inclusão
│   ├── views/            # Visualizações
│   └── index.php         # Página principal
├── instructor/           # Área do formador
│   ├── includes/
│   ├── views/
│   └── index.php
├── student/              # Área do estudante
│   ├── includes/
│   ├── views/
│   └── index.php
├── assets/               # Recursos estáticos
│   ├── css/
│   ├── js/
│   ├── img/
│   └── uploads/
├── configs/              # Configurações
│   └── config.php
├── includes/             # Includes globais
│   ├── auth.php
│   ├── functions.php
│   ├── header.php
│   ├── footer.php
│   └── logout.php
├── pages/                # Páginas públicas
│   ├── auth/
│   └── *.php
├── uploads/              # Uploads de usuários
├── index.php             # Página inicial
├── instalacao.php        # Instalador
├── database.sql          # Estrutura do banco de dados
└── .htaccess            # Regras do Apache
```

## Configuração

### Configurações Principais

Edite o arquivo `configs/config.php` para configurar:

- Conexão com banco de dados
- Configurações de email
- Configurações do site
- Chaves de API para pagamentos

### Configurações de Pagamento

Configure os métodos de pagamento em `configs/config.php`:

- M-Pesa: Número da conta e credenciais
- e-Mola: Credenciais da API
- mKesh: Configurações
- PayPal: Client ID e Secret

## Utilização

### Administradores

1. Acessar `/admin/` 
2. Gerir utilizadores, cursos, configurações
3. Visualizar relatórios e estatísticas

### Formadores

1. Acessar `/instructor/`
2. Criar e gerir cursos
3. Acompanhar progresso dos estudantes

### Estudantes

1. Registar-se ou fazer login
2. Navegar e inscrever-se em cursos
3. Acessar `/student/` para ver cursos e progresso

## Segurança

- Todas as passwords são hashadas com bcrypt
- Proteção contra SQL injection
- Proteção contra XSS
- Uploads validados e restritos
- SSL recomendado para produção

## Suporte

Para suporte técnico, contacte:

- Email: carsaimozambique@gmail.com
- WhatsApp: +258 86 241 4345
- Telefone: +258 84 441 4345

## Licença

Este software é propriedade da Carsai Mozambique. Todos os direitos reservados.

## Desenvolvido por

**CarsaiDev** - Desenvolvimento de Software  
[carimosaidempinda@gmail.com](mailto:carimosaidempinda@gmail.com)  
[+258 84 441 4345](tel:+258844414345)
