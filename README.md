<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GoodCard - Aprovação</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            'goodcard-orange': '#FF6B35',
            'goodcard-navy': '#1A2B4C',
            'goodcard-gray': '#F5F7FA',
            'goodcard-green': '#10B981',
          }
        }
      }
    }
  </script>
  <style>
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .animate-fade-in { 
      animation: fadeIn 0.6s ease-out; 
    }
    @keyframes pulse {
      0%, 100% { opacity: 1; }
      50% { opacity: .5; }
    }
    .animate-pulse { 
      animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite; 
    }
  </style>
</head>
<body>
  <div class="min-h-screen bg-white">
    <!-- CABEÇALHO -->
    <header class="fixed top-0 left-0 right-0 bg-white shadow-sm z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
        <div class="flex items-center gap-3">
          <div class="text-2xl font-bold text-goodcard-orange">GoodCard</div>
          <div class="text-sm text-goodcard-navy">Cartão de Crédito para Combustível</div>
        </div>
      </div>
    </header>

    <!-- SEÇÃO HERO - APROVAÇÃO -->
    <section class="pt-24 pb-12 bg-gradient-to-br from-orange-50 to-orange-100">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center animate-fade-in">
          <div class="flex justify-center mb-6">
            <i data-lucide="check-circle-2" class="w-24 h-24 text-goodcard-green animate-pulse"></i>
          </div>
          <h1 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-goodcard-navy mb-4">
            Parabéns! Sua análise foi concluída
          </h1>
          <p class="text-xl sm:text-2xl text-goodcard-navy opacity-80">
            Você foi aprovado para o cartão GoodCard Combustível
          </p>
        </div>
      </div>
    </section>

    <!-- SEÇÃO LIMITE -->
    <section class="py-12 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-2xl mx-auto">
          <div class="bg-white border-4 border-goodcard-orange rounded-xl shadow-lg p-8 text-center animate-fade-in">
            <div class="text-5xl sm:text-6xl font-bold text-goodcard-orange mb-4">
              R$ 3.500,00
            </div>
            <p class="text-xl text-goodcard-navy font-semibold">
              Válido em TODOS os postos do Brasil
            </p>
            <div class="flex justify-center gap-4 mt-6">
              <div class="w-16 h-10 bg-red-600 rounded flex items-center justify-center text-white text-xs font-bold">
                SHELL
              </div>
              <div class="w-16 h-10 bg-yellow-500 rounded flex items-center justify-center text-white text-xs font-bold">
                IPIRANGA
              </div>
              <div class="w-20 h-10 bg-blue-800 rounded flex items-center justify-center text-white text-xs font-bold">
                PETROBRAS
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SEÇÃO BENEFÍCIOS -->
    <section class="py-12 bg-goodcard-gray">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <!-- Card 1 - Cartão Físico -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
            <div class="flex justify-center mb-4">
              <div class="bg-goodcard-green bg-opacity-10 rounded-full p-4">
                <i data-lucide="credit-card" class="w-8 h-8 text-goodcard-green"></i>
              </div>
            </div>
            <h3 class="text-xl font-bold text-goodcard-navy mb-2 text-center">
              Cartão Físico
            </h3>
            <p class="text-goodcard-navy opacity-70 text-center">
              Seu cartão é físico e aceito em qualquer bomba de combustível do país
            </p>
          </div>

          <!-- Card 2 - Sem Anuidade -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
            <div class="flex justify-center mb-4">
              <div class="bg-goodcard-green bg-opacity-10 rounded-full p-4">
                <i data-lucide="ban" class="w-8 h-8 text-goodcard-green"></i>
              </div>
            </div>
            <h3 class="text-xl font-bold text-goodcard-navy mb-2 text-center">
              Sem Anuidade
            </h3>
            <p class="text-goodcard-navy opacity-70 text-center">
              Você não paga nada para manter seu cartão ativo. Zero tarifas anuais
            </p>
          </div>

          <!-- Card 3 - Você Define a Data -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
            <div class="flex justify-center mb-4">
              <div class="bg-goodcard-green bg-opacity-10 rounded-full p-4">
                <i data-lucide="calendar" class="w-8 h-8 text-goodcard-green"></i>
              </div>
            </div>
            <h3 class="text-xl font-bold text-goodcard-navy mb-2 text-center">
              Você Define a Data
            </h3>
            <p class="text-goodcard-navy opacity-70 text-center">
              Escolha o melhor dia de fechamento da fatura após desbloquear seu cartão no app
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- SEÇÃO ENVIO -->
    <section class="py-12 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-2xl mx-auto">
          <div class="bg-white border-2 border-goodcard-orange border-opacity-30 rounded-xl shadow-lg p-8 animate-fade-in">
            <div class="flex items-start gap-4">
              <div class="bg-goodcard-orange bg-opacity-10 rounded-full p-3">
                <i data-lucide="truck" class="w-8 h-8 text-goodcard-orange"></i>
              </div>
              <div class="flex-1">
                <h2 class="text-2xl font-bold text-goodcard-navy mb-4">
                  Receba seu cartão em casa
                </h2>
                <p class="text-lg text-goodcard-navy mb-2">
                  Faça o pagamento de apenas <span class="font-bold text-goodcard-orange">R$ 1,00</span> para despacho/envio
                </p>
                <p class="text-lg text-goodcard-navy font-semibold">
                  Receba em até <span class="text-goodcard-orange">7 dias úteis</span>, independente do seu estado!
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SEÇÃO PIX - CTA PRINCIPAL -->
    <section class="py-12 bg-goodcard-gray">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-2xl mx-auto">
          <div class="bg-goodcard-orange rounded-xl shadow-xl p-8 text-center animate-fade-in">
            <h2 class="text-2xl sm:text-3xl font-bold text-white mb-6">
              Garanta seu cartão agora
            </h2>
            <button
              id="pixButton"
              class="w-full sm:w-auto px-8 py-4 bg-white text-goodcard-orange rounded-lg font-bold text-lg flex items-center justify-center gap-3 mx-auto hover:bg-gray-100 transition-colors shadow-lg"
            >
              <i data-lucide="copy" class="w-6 h-6"></i>
              <span id="pixButtonText">COPIAR CHAVE PIX</span>
            </button>
            <p id="pixMessage" class="mt-4 text-white font-semibold animate-fade-in hidden">
              Chave copiada! Abra seu banco → PIX → CNPJ
            </p>
            <div class="mt-6 pt-6 border-t border-white border-opacity-30">
              <p class="text-white opacity-90 text-sm mb-2">Chave PIX (CNPJ):</p>
              <p class="text-white text-xl font-mono font-bold">
                10.956.143/0001-25
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- DADOS DO PAGAMENTO -->
    <section class="py-8 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-2xl mx-auto">
          <div class="bg-goodcard-gray rounded-lg p-6">
            <p class="text-sm text-goodcard-navy opacity-70 mb-2">Dados que aparecerão no PIX:</p>
            <div class="space-y-1 text-sm text-goodcard-navy">
              <p><span class="font-semibold">Nome:</span> GOOD CARD</p>
              <p><span class="font-semibold">CNPJ:</span> 10.956.143/0001-25</p>
              <p><span class="font-semibold">Instituição:</span> Itaú Unibanco S.A.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- RODAPÉ -->
    <footer class="py-6 bg-goodcard-navy">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <p class="text-center text-white opacity-80 text-sm">
          GoodCard © 2026 - Cartão de Crédito para Combustível
        </p>
      </div>
    </footer>
  </div>

  <script>
    // Inicializar ícones do Lucide
    lucide.createIcons();

    // Função para copiar chave PIX
    const pixButton = document.getElementById('pixButton');
    const pixButtonText = document.getElementById('pixButtonText');
    const pixMessage = document.getElementById('pixMessage');
    const pixKey = '10956143000125';

    pixButton.addEventListener('click', function() {
      // Copiar para clipboard
      navigator.clipboard.writeText(pixKey).then(function() {
        // Mudar texto do botão
        pixButtonText.textContent = 'Chave Copiada!';
        
        // Mudar cor do botão
        pixButton.classList.remove('bg-white', 'text-goodcard-orange', 'hover:bg-gray-100');
        pixButton.classList.add('bg-goodcard-green', 'text-white');
        
        // Mostrar mensagem
        pixMessage.classList.remove('hidden');
        
        // Mudar ícone
        const icon = pixButton.querySelector('i');
        icon.setAttribute('data-lucide', 'check');
        lucide.createIcons();
        
        // Resetar após 3 segundos
        setTimeout(function() {
          pixButtonText.textContent = 'COPIAR CHAVE PIX';
          pixButton.classList.remove('bg-goodcard-green', 'text-white');
          pixButton.classList.add('bg-white', 'text-goodcard-orange', 'hover:bg-gray-100');
          pixMessage.classList.add('hidden');
          icon.setAttribute('data-lucide', 'copy');
          lucide.createIcons();
        }, 3000);
      }).catch(function(err) {
        console.error('Erro ao copiar:', err);
        alert('Erro ao copiar chave PIX. Por favor, copie manualmente: ' + pixKey);
      });
    });
  </script>
</body>
</html>
