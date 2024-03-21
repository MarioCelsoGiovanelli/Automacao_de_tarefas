![Badge Concluido](http://img.shields.io/static/v1?label=STATUS&message=%20CONCLUIDO&color=GREEN&style=for-the-badge)
# :robot: Automação de Tarefas

  Com a biblioteca **yfinance** é possível obter os dados de ações de forma automática. O **[Yahho Finanças](http://br.financas.yahoo.com/)** é um site que fornece notícias sobre finanças, incluindo cotações de ações.

  Com essa automação podemos buscar dados das ações automaticamente utilizando a biblioteca **yfinance**, realizar as análises dos dados encontrados e gerar estatísticas, gráficos, automatizar o controle do teclado e mouse com o **pyautogui**, utilizar strings de múltiplas linhas e enviar automaticamente o e-mail com o resultado da análise.


:movie_camera:

<img src=".\Animação.gif" alt="Código funcionando" width="600px" heidth="400px">

  Usando a função **input()** para receber o código da ação
````python
ticker = input('Digite o código da ação: ')
````
  Para imprimir os dados da ação utilizamos o método **.history()** depois da variável que armazena as informações.
````python
dados = yfinance.Ticker(ticker)
dados.history()
````

|             | Open          | High  |
| ------------- |:-------------:| -----:|
| Date     |                 |       |
| 2024-02-21 00:00:00-03:00      | 42.450001      |   42.720001|
| 2024-02-22 00:00:00-03:00 | 42.669998  |    42.680000|
|2024-02-23 00:00:00-03:00	|42.139999|	42.240002|
| 2024-02-26 00:00:00-03:00 |	41.900002|	42.730000|
|2024-02-27 00:00:00-03:00	|42.700001	|42.820000|
|2024-03-01 00:00:00-03:00	|40.349998	|40.849998|
|2024-03-04 00:00:00-03:00	|40.270000	|40.750000|

  Para configurar por um período histórico usamos para ano: **y**, mês: **mo** e dia: **d**
````python
Tabela = dados.history(“6mo”)
````
  Para selecionar apenas a coluna desejada, basta colocar o nome dela entre colchetes na frente da variável que está armazenando os dados
````python
Fechamento = tabela.Close
````

Date

2023-09-21 00:00:00-03:00  |  32.501633

2023-09-22 00:00:00-03:00  |  32.761570

2023-09-25 00:00:00-03:00  |  32.973370

2023-09-26 00:00:00-03:00  |  32.212814

2023-09-27 00:00:00-03:00  |  33.233307

                               ...    
                               
2024-03-15 00:00:00-03:00  |  36.320000

2024-03-18 00:00:00-03:00  |  36.340000

2024-03-19 00:00:00-03:00  |  36.070000

2024-03-20 00:00:00-03:00  |  36.700001

2024-03-21 00:00:00-03:00  |  36.070000




:keyboard:  Utilizando a biblioteca **pyautogui** podemos criar as mesmas ações do teclado
````python
Pyautogui.hotkey(“ctrl”, “t”)
Pyautogui.hotkey(“enter”)
````
:pager:  Com a biblioteca **pyperclip** podemos criar ações como copiar e colar mensagens
````python
Pyperclip.copy(“email@email.com”)
Pyperclip.copy(“Análise de dados”)
````
:computer_mouse:  Algumas ações como clicar com o mouse em botões pode ser feita com o seguinte método 
````python
pyautogui.click(x=0, y=0)
````


## :computer: Técnicas e Tecnologias utilizadas:
- Buscar dados automaticamente
- Gerar estatísticas
- Gerar gráfico
- Automatizar o controle do teclado e mouse
- Enviar e-mails de forma automática
  
  - Jupyter notebook

### :books: Bibliotecas:
 - yfinance

 - pyautogui

 - pyperclip
