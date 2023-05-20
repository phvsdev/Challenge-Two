<p align="center">
  <h1 align="center">DevOps - Challenge Two</h1>
</p>

## Deploy Site do Desafio em EC2 na AWS utilizando o Terraform, Docker. 

  <img align="right" alt="GIF" src="https://github.com/abhisheknaiidu/abhisheknaiidu/blob/master/code.gif?raw=true" width="500" height="320" />

Neste desafio DevOps, você será desafiado a criar e configurar uma instância EC2 na no Cloud Provider Amazon Web Services (AWS), instalar o Docker nessa instância e realizar o deploy de um código contido nesse repositório, tudo isso utilizando o [Terraform](https://www.terraform.io/).

**Passo 1: Criação da instância EC2**

Utilize o Terraform para definir a configuração da instância EC2, juntamente com os recursos de rede necessários, como as sub-redes, grupos de segurança e rotas. Você pode utilizar o provedor da AWS no Terraform para criar esses recursos. 

Certifique-se de configurar corretamente a conectividade com a internet e verifique o tipo de instância adequado às necessidades do projeto `free tier da aws` e caso não esteja utilizando uma Amazon Machine Images configure corretamente o [AWS SSM](https://docs.aws.amazon.com/pt_br/systems-manager/latest/userguide/sysman-manual-agent-install.html) para acesso tanto via Terminal com Keypar quanto o SSM AWS. 

**Passo 2: Instalação do Docker utilizando Terraform**

Utilize o Terraform para executar um script de provisionamento que instale o Docker na instância EC2. O script de provisionamento pode ser fornecido como parte da configuração do recurso da instância EC2 no Terraform. Certifique-se de usar o script apropriado para a distribuição Linux escolhida. 

**Passo 3: Liberação de tráfego para a internet**

Por padrão, as instâncias EC2 têm algumas restrições de tráfego para garantir a segurança. No entanto, para permitir que a aplicação seja acessada pela internet, você precisará configurar as regras de segurança (grupos de segurança) para liberar as portas necessárias. Certifique-se de abrir as portas adequadas para o acesso externo à aplicação ou somente ao seu IP.

Utilize o Terraform para configurar as regras de segurança (grupos de segurança) para permitir o tráfego necessário. Você pode definir as regras de segurança no recurso de grupo de segurança associado à instância EC2. Certifique-se de abrir as portas adequadas para o acesso externo à aplicação ou somente ao seu IP.

**Passo 4: Deploy do código zipado em um container**

Neste último passo, você deverá realizar o deploy do código neste repositório em um container Docker na instância EC2. 

Utilize o Terraform para copiar o código zipado para a instância EC2. Você pode usar o recurso null_resource no Terraform para executar comandos na instância EC2, como copiar arquivos. 

Em seguida, utilize o Dockerfile para definir o ambiente de execução e as dependências necessárias para a aplicação. Utilize o recurso null_resource novamente para executar comandos Docker, como docker build e docker run, para buildar e executar um contêiner com a aplicação.



**Passo 5: Envio das evidências no Discord**

Nesta última etapa você irá enviar o código do Terraform encapsulado em um arquivo comprimido e a url página web que abre após o deploy do código.

A evidência que a app está rodando na EC2 será igual essa página: https://phvsdev.github.io/Challenge-Two/


Ao final deste desafio, você terá demonstrado suas habilidades em DevOps, mostrando a capacidade de configurar uma instância EC2 utilizando o Terraform, instalar o Docker, liberar o tráfego necessário e realizar o deploy de um código em um container tudo utilizando IaC. Isso reflete um cenário comum na prática DevOps, onde a automatização e a orquestração de infraestrutura são fundamentais para o desenvolvimento e implantação de aplicações modernas e escaláveis.

  <img align="center" alt="GIF" src="https://www.datocms-assets.com/2885/1620155439-blog-library-product-terraform-aws-logomarks.jpg"/>

<p></p>

## Lembre-se de que é necessário ter o Terraform instalado e configurado corretamente, com as credenciais da AWS adequadas para provisionar os recursos na nuvem. Além disso, certifique-se de que os scripts de provisionamento e os arquivos necessários estejam disponíveis no momento da execução do Terraform.
