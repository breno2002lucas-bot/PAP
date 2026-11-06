# Gestão de Leads — Projeto Operação PAP Cujubim

Projeto web para PAP, Pesquisa de Bairro, Panfletagem por Rua, Propaganda Volante, Ações/Eventos, Vendas e Gestão de Usuários.

## Implantação
1. Crie um projeto em https://supabase.com e execute `schema.sql` no SQL Editor.
2. Em Authentication > Providers, habilite Email. Desative cadastro público no projeto para que somente administradores criem contas pelo painel do Supabase.
3. Crie a primeira conta em Authentication > Users e promova seu UUID a `admin` com o comando no fim do SQL.
4. Copie `.env.example` para `.env` e preencha URL e chave **anon/publishable** (nunca a service_role).
5. Execute `npm install` e `npm run dev` para testar. Para produção, importe o repositório na Vercel, configure as mesmas variáveis de ambiente e faça deploy.
6. Crie usuários em Authentication > Users; o gatilho cria perfis `field` automaticamente. Um administrador altera perfis na tela Usuários.

## Segurança e limitações
- O controle de acesso é aplicado por Row Level Security no banco; o menu sozinho não é controle de segurança.
- Colaboradores veem apenas seus próprios registros; supervisor, gerente e administrador veem registros gerais.
- Não é um site já publicado: exige configuração de Supabase e hospedagem.
- Esta é uma primeira versão funcional (MVP), sem recuperação de senha customizada, anexos de fotos, edição de registros, vínculo automático entre eventos e leads ou auditoria detalhada. Configure políticas de privacidade e retenção antes de coletar dados pessoais reais.

## Identidade do sistema
Nome: Gestão de Leads. Subtítulo: Projeto Operação PAP Cujubim. Não há senha fixa no código.
