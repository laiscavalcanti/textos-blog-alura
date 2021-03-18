# Tutorial de como conectar o Github via SSH!

1 - Utilizar o protocolo SSH no momento de adicionar o repositório.

ex: git remote add origin < end ssh >

2 - git add .

3 -  git commit -m " "

4 -  git push -u origin master

No site do github, no seu perfil vá em: 
- Settings >  Gerating SSH Key >  Gerating a new SSH Key and adding it to the shh-agent

5 - Vá até o seu terminal e utilize o comando : ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
Substitua pelo seu email de cadastro no Github. E então, ele irpa perguntar onde você quer gerar a chave rsa. O caminho vai ser mostrado, o padrão é aceitar o sugestão de local, mas caso você queira, você pode mudar. Mas como queremos salvar onde está a sugestão, apertamos enter.

6 - Senha: Após isso ele solicitará uma seha, não é obrigatório colocar. Ela sempre será solicitada quando comando como, git push, git pull, git merge forem dados

7 - Em seguida aparecerá uma imagem com a key que foi gerada. 

8 -  Agora vamos navegar até o caminho que ele nós deu no passo 5.

9 - Nagegue até a pasta .ssh, é uma pasta oculta. Dentro dessa pasta contém duas pastas com as chaves puplica e a privada.

10 - Voltamos ao github e iremos novamente SSH KEys e clicamos em New SSH KEYS. Coloque o título da sua chave. Geralmente, algo que identifique, como PC HOME, PC OFFICE

11- Em seguida, damos o comenado 
`cat id_rsa.pub`