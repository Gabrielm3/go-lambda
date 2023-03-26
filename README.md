<h1>AWS Lambda Function em Go</h1>

<div>
    <img src="https://github.com/Gabrielm3/go-lambda/blob/master/go.svg" alt="Go">
</div>


<h2>Executando o código</h2>
<ol>
  <li>Clone este repositório para a sua máquina</li>
  <li>No terminal, vá para o diretório do projeto e execute o comando <code>go build main.go</code></li>
  <li>Crie um pacote zip da função com o seguinte comando: <code> zip function.zip main</code></li>
  <li>Crie a função no AWS Lambda com o seguinte comando:<br>
  <code> aws lambda create-function \
  --function-name my-function \
  --zip-file fileb://function.zip \
  --handler main \
  --runtime go1.x \
  --role arn:aws:iam::YOUR_ROLE:role/lambda-role</code></li>
  <li>Teste a função com o seguinte comando:<br>
  <code>aws lambda invoke --function-name lambda-function</code></li>
</ol>

<h2>Uso</h2>
<div>Para usar a função Lambda, basta invocá-la usando o AWS CLI ou outra ferramenta que suporte o AWS Lambda.</div>
