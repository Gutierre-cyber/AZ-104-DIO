Passo a Passo: Criação da Máquina Virtual
Siga as etapas abaixo para provisionar sua VM no Azure.

1. Acessar o Portal do Azure
Abra seu navegador e navegue até o Portal do Azure: portal.azure.com.

Faça login com suas credenciais da conta Azure.

2. Iniciar a Criação da Máquina Virtual
Na página inicial do Portal do Azure, procure por "Máquinas virtuais" na barra de pesquisa superior e selecione "Máquinas virtuais" nos resultados.

Clique em "+ Criar" ou "Criar máquina virtual".

3. Configurar os Detalhes Básicos (Guia "Básico")
Esta é a primeira seção de configurações.

Assinatura: Escolha sua assinatura Azure.

Grupo de recursos: Crie um novo grupo de recursos (ex: rg-minhavm) ou selecione um existente. Um grupo de recursos é um contêiner lógico para seus recursos do Azure.

Nome da máquina virtual: Dê um nome único para sua VM (ex: minha-primeira-vm).

Região: Selecione a região geográfica mais próxima de você para otimizar a latência (ex: Brazil South).

Opções de disponibilidade: Para este guia simples, você pode deixar como "Nenhuma redundância de infraestrutura necessária".

Tipo de segurança: Mantenha "Standard" ou "Máquinas virtuais confiáveis" para segurança aprimorada.

Imagem: Escolha o sistema operacional para sua VM (ex: Windows Server 2019 Datacenter ou Ubuntu Server 22.04 LTS).

Tamanho: Selecione o tamanho da VM (ex: Standard_B2s é um bom ponto de partida para testes, oferecendo 2 vCPUs e 4 GB de RAM). O Azure sugerirá um tamanho com base na imagem escolhida.

Nome de usuário: Crie um nome de usuário para acessar a VM (ex: adminuser).

Senha: Crie e confirme uma senha forte. Anote esta senha, você precisará dela para acessar a VM!

Regras de porta de entrada pública:

Para Windows: Selecione "Permitir portas selecionadas" e escolha "RDP (3389)".

Para Linux: Selecione "Permitir portas selecionadas" e escolha "SSH (22)".

Aviso de Segurança: Permitir RDP/SSH diretamente da internet não é recomendado para ambientes de produção. Para este guia, estamos simplificando o acesso.

4. Configurar Discos (Guia "Discos")
Tipo de disco de SO: Escolha o tipo de disco para o sistema operacional. Para a maioria dos casos, "SSD Standard" é suficiente para começar e é mais econômico que o Premium SSD.

Você pode deixar as outras configurações padrão para este guia.

5. Configurar Rede (Guia "Rede")
Rede virtual: O Azure criará uma nova rede virtual (VNet) e sub-rede por padrão. Você pode aceitar os padrões para este guia.

IP público: O Azure atribuirá um IP público à sua VM para acesso externo.

Grupo de segurança de rede (NSG): O NSG gerenciará as regras de tráfego de entrada e saída. Mantenha "Básico" para este guia.

Portas de entrada públicas: Confirme que as portas necessárias (RDP/SSH) estão selecionadas conforme configurado na seção "Básico".

Deixe as demais configurações padrão.

6. Configurar Gerenciamento (Guia "Gerenciamento")
Você pode deixar as configurações padrão nesta guia para este guia rápido. Se quiser mais detalhes, explore as opções como monitoramento e diagnóstico de inicialização.

7. Tags (Guia "Tags")
Opcional, mas útil para organização e faturamento. Você pode adicionar pares chave-valor (ex: Ambiente: Desenvolvimento).

8. Revisar e Criar (Guia "Revisar + criar")
Revise todas as configurações selecionadas.

O Azure executará uma validação para garantir que todas as configurações estão corretas. Se houver algum erro, ele será indicado aqui.

Após a validação ser aprovada, clique no botão "Criar".

A implantação da sua VM levará alguns minutos. Você pode acompanhar o progresso no painel de notificações do Azure.

Acessando a Máquina Virtual
Assim que a implantação for concluída, você poderá acessar sua VM.

1. Obter o IP Público da VM
Após a implantação, clique em "Ir para o recurso" na notificação de implantação, ou navegue até "Máquinas virtuais" e clique no nome da sua VM.

Na página de visão geral da VM, localize o Endereço IP público. Anote este endereço.

2. Conectar-se à VM
Para Máquinas Virtuais Windows (via RDP):

Abra o "Conexão de Área de Trabalho Remota" (pesquise por mstsc no Windows).

No campo "Computador", digite o IP público da sua VM.

Clique em "Conectar".

Quando solicitado, insira o nome de usuário e a senha que você configurou durante a criação da VM.

Aceite o certificado de segurança se aparecer.

Para Máquinas Virtuais Linux (via SSH):

Abra um terminal (Linux/macOS) ou use um cliente SSH como PuTTY (Windows).

Use o comando SSH:

Bash

ssh <seu_nome_de_usuario>@<IP_publico_da_VM>
Exemplo: ssh adminuser@20.123.45.678

Quando solicitado, digite a senha que você configurou para o usuário.

