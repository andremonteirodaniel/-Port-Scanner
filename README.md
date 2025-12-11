# -Port-Scanner
```markdown
# 🌐 Port Scanner Simples (TCP)

Um script de varredura de portas em Python usando a biblioteca `socket` nativa. Ele verifica a disponibilidade de portas TCP em um host alvo, ajudando a identificar serviços em execução.

## ✨ Funcionalidades

* **Varredura TCP:** Utiliza `socket.connect_ex` para tentar a conexão com portas específicas, ideal para varredura rápida.
* **Timeout Configurado:** Define um timeout de 0.5 segundos para cada tentativa de conexão para otimizar a velocidade.
* **Portas Padrão:** Se nenhuma porta for especificada, ele varre uma lista de portas comuns (21, 22, 23, 25, 80, 443, 445, 8080, 8443, 3306, 139, 135).
* **Saída Simples:** Imprime a porta com o status "[+] <PORTA> open" se a conexão for bem-sucedida (código de retorno 0).

## ⚙️ Pré-requisitos

Esta ferramenta usa apenas a biblioteca `socket` e `sys` que são nativas do Python. Nenhuma instalação adicional é necessária.

## 📦 Instalação

1.  Clone o repositório:
    ```bash
    git clone https://github.com/andremonteirodaniel/-Port-Scanner.git
    cd -Port-Scanner

## 🚀 Uso

### Opção 1: Usando portas padrão

Forneça apenas o host alvo. A lista de portas padrão será utilizada.

```bash
python portscan.py <HOST_ALVO>
# Exemplo: python portscan.py google.com

### Opção 2: Especificando portas
Forneça o host alvo e uma lista de portas separadas por vírgulas (sem espaços).

'''bash
python portscan.py <HOST_ALVO> <PORTAS_COM_VIRGULA>
# Exemplo: python portscan.py google.com 22,80,443,8080

### **Detalhes Técnicos Importantes**

* A varredura usa `socket.connect_ex()`. Um retorno de código `0` indica que a porta está aberta.
* O *timeout* é definido como `0.5` segundos por tentativa.
* Se nenhuma porta for fornecida, a lista padrão inclui: `21, 22, 23, 25, 80, 443, 445, 8080, 8443, 3306, 139, 135`.
