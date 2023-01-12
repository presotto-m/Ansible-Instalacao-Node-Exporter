# Instalar node exporter utilizando ansible playbook


<img alt="Ansible Collection" src="https://img.shields.io/badge/Ansible-Ansible%20Playbook-blue"> <img alt="Prometheus" src="https://img.shields.io/badge/Prometheus-Node%20Exporter-orange">

Playbook para realizar a instalação do node exporter em servidores linux utilizando o systemD

Para utilizar o playbook o ansible deve estar instalado corretamente.

### Baixando os arquivos do repositório

```
cd /tmp
git clone https://github.com/GabrielHespanhol/InstallNodeExporter.git
cd InstallNodeExporter
```

### Executando o playbook

Primeiro adicione o IP dos servidores no arquivos hosts

Após adicionar o IP dos servidores no arquivos hosts basta executar o comando
```
ansible-playbook -i hosts playbook.yml -K
```

### Observações

* Arquivo hosts contem os endereços de servidores para execução do playbook
* Opção -K é para solicitar a senha de root dos servidores que serão acessados para configuração do node exporter
* O playbook foi construido e testado apenas em servidores linux debian
