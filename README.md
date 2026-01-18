<!doctype html>
<html lang="pt-br">
<head>
<meta charset="utf-8">
<title>GoodCard – Cartão Combustível Aprovado</title>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
body{font-family:Arial;background:#f3f3f3;text-align:center;padding:20px;color:#333}
h1{color:#003366;font-size:24px}
.limite{font-size:42px;color:#ff6600;margin:10px 0}
.btn{display:inline-block;background:#ff6600;color:#fff;padding:14px 28px;border-radius:4px;font-size:18px;margin-top:20px;border:none;cursor:pointer}
small{display:block;margin-top:15px;font-size:12px;color:#666}
</style>
</head>
<body>
<h1>Cartão exclusivo para combustível <strong>aprovado!</strong></h1>
<p class="limite"><strong>R$ 3.500,00</strong></p>
<p>de limite para abastecimento em <strong>todos os postos do Brasil</strong>, sem restrição de bandeira.</p>
<ul style="text-align:left;display:inline-block">
  <li>Somente uso <strong>físico</strong> – não perca o plástico.</li>
  <li>Aceito em <strong>qualquer bomba de gasolina</strong>.</li>
  <li>Sem anuidade, sem juros rotativos.</li>
</ul>
<p>Para envio do cartão ao seu endereço em até <strong>5 dias úteis</strong>, pague apenas a taxa de postagem:</p>
<button class="btn" onclick="copiar()">Copiar chave PIX</button>
<small>
  CNPJ: 10.956.143/0001-25 | Instituição: Itaú Unibanco S.A.<br>
  Protocolo gerado automaticamente – não é necessário reembolso.
</small>
<script>
function copiar(){
  var chave = "10956143000125";          // só números
  navigator.clipboard.writeText(chave);
  alert("Chave copiada! Agora abra seu banco, escolha PIX → CNPJ e cole.");
}
</script>
</body>
</html>
