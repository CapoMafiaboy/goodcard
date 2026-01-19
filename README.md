import { useState } from 'react'
import { 
  CheckCircle2, 
  CreditCard, 
  Ban, 
  Calendar, 
  Truck, 
  Copy,
  Check
} from 'lucide-react'

function App() {
  const [pixCopied, setPixCopied] = useState(false)

  const handleCopyPix = () => {
    const pixKey = '10956143000125'
    navigator.clipboard.writeText(pixKey).then(() => {
      setPixCopied(true)
      setTimeout(() => {
        setPixCopied(false)
      }, 3000)
    })
  }

  return (
    <div className="min-h-screen bg-white">
      {/* CABEÇALHO */}
      <header className="fixed top-0 left-0 right-0 bg-white shadow-sm z-50">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
          <div className="flex items-center gap-3">
            <div className="text-2xl font-bold text-goodcard-orange">GoodCard</div>
            <div className="text-sm text-goodcard-navy">Cartão de Crédito para Combustível</div>
          </div>
        </div>
      </header>

      {/* SEÇÃO HERO - APROVAÇÃO */}
      <section className="pt-24 pb-12 bg-gradient-to-br from-orange-50 to-orange-100">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center animate-fade-in">
            <div className="flex justify-center mb-6">
              <CheckCircle2 
                className="w-24 h-24 text-goodcard-green animate-pulse" 
                strokeWidth={1.5}
              />
            </div>
            <h1 className="text-3xl sm:text-4xl lg:text-5xl font-bold text-goodcard-navy mb-4">
              Parabéns! Sua análise foi concluída
            </h1>
            <p className="text-xl sm:text-2xl text-goodcard-navy/80">
              Você foi aprovado para o cartão GoodCard Combustível
            </p>
          </div>
        </div>
      </section>

      {/* SEÇÃO LIMITE */}
      <section className="py-12 bg-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="max-w-2xl mx-auto">
            <div className="bg-white border-4 border-goodcard-orange rounded-xl shadow-lg p-8 text-center animate-fade-in">
              <div className="text-5xl sm:text-6xl font-bold text-goodcard-orange mb-4">
                R$ 3.500,00
              </div>
              <p className="text-xl text-goodcard-navy font-semibold">
                Válido em TODOS os postos do Brasil
              </p>
              <div className="flex justify-center gap-4 mt-6">
                <div className="w-16 h-10 bg-red-600 rounded flex items-center justify-center text-white text-xs font-bold">
                  SHELL
                </div>
                <div className="w-16 h-10 bg-yellow-500 rounded flex items-center justify-center text-white text-xs font-bold">
                  IPIRANGA
                </div>
                <div className="w-20 h-10 bg-blue-800 rounded flex items-center justify-center text-white text-xs font-bold">
                  PETROBRAS
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* SEÇÃO BENEFÍCIOS */}
      <section className="py-12 bg-goodcard-gray">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
            {/* Card 1 - Cartão Físico */}
            <div className="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
              <div className="flex justify-center mb-4">
                <div className="bg-goodcard-green/10 rounded-full p-4">
                  <CreditCard className="w-8 h-8 text-goodcard-green" />
                </div>
              </div>
              <h3 className="text-xl font-bold text-goodcard-navy mb-2 text-center">
                Cartão Físico
              </h3>
              <p className="text-goodcard-navy/70 text-center">
                Seu cartão é físico e aceito em qualquer bomba de combustível do país
              </p>
            </div>

            {/* Card 2 - Sem Anuidade */}
            <div className="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
              <div className="flex justify-center mb-4">
                <div className="bg-goodcard-green/10 rounded-full p-4">
                  <Ban className="w-8 h-8 text-goodcard-green" />
                </div>
              </div>
              <h3 className="text-xl font-bold text-goodcard-navy mb-2 text-center">
                Sem Anuidade
              </h3>
              <p className="text-goodcard-navy/70 text-center">
                Você não paga nada para manter seu cartão ativo. Zero tarifas anuais
              </p>
            </div>

            {/* Card 3 - Você Define a Data */}
            <div className="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-shadow animate-fade-in">
              <div className="flex justify-center mb-4">
                <div className="bg-goodcard-green/10 rounded-full p-4">
                  <Calendar className="w-8 h-8 text-goodcard-green" />
                </div>
              </div>
              <h3 className="text-xl font-bold text-goodcard-navy mb-2 text-center">
                Você Define a Data
              </h3>
              <p className="text-goodcard-navy/70 text-center">
                Escolha o melhor dia de fechamento da fatura após desbloquear seu cartão no app
              </p>
            </div>
          </div>
        </div>
      </section>

      {/* SEÇÃO ENVIO */}
      <section className="py-12 bg-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="max-w-2xl mx-auto">
            <div className="bg-white border-2 border-goodcard-orange/30 rounded-xl shadow-lg p-8 animate-fade-in">
              <div className="flex items-start gap-4">
                <div className="bg-goodcard-orange/10 rounded-full p-3">
                  <Truck className="w-8 h-8 text-goodcard-orange" />
                </div>
                <div className="flex-1">
                  <h2 className="text-2xl font-bold text-goodcard-navy mb-4">
                    Receba seu cartão em casa
                  </h2>
                  <p className="text-lg text-goodcard-navy mb-2">
                    Faça o pagamento de apenas <span className="font-bold text-goodcard-orange">R$ 1,00</span> para despacho/envio
                  </p>
                  <p className="text-lg text-goodcard-navy font-semibold">
                    Receba em até <span className="text-goodcard-orange">7 dias úteis</span>, independente do seu estado!
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* SEÇÃO PIX - CTA PRINCIPAL */}
      <section className="py-12 bg-goodcard-gray">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="max-w-2xl mx-auto">
            <div className="bg-goodcard-orange rounded-xl shadow-xl p-8 text-center animate-fade-in">
              <h2 className="text-2xl sm:text-3xl font-bold text-white mb-6">
                Garanta seu cartão agora
              </h2>
              <button
                onClick={handleCopyPix}
                className={`w-full sm:w-auto px-8 py-4 bg-white text-goodcard-orange rounded-lg font-bold text-lg flex items-center justify-center gap-3 mx-auto hover:bg-gray-100 transition-colors shadow-lg ${
                  pixCopied ? 'bg-goodcard-green text-white' : ''
                }`}
              >
                {pixCopied ? (
                  <>
                    <Check className="w-6 h-6" />
                    Chave Copiada!
                  </>
                ) : (
                  <>
                    <Copy className="w-6 h-6" />
                    COPIAR CHAVE PIX
                  </>
                )}
              </button>
              {pixCopied && (
                <p className="mt-4 text-white font-semibold animate-fade-in">
                  Chave copiada! Abra seu banco → PIX → CNPJ
                </p>
              )}
              <div className="mt-6 pt-6 border-t border-white/30">
                <p className="text-white/90 text-sm mb-2">Chave PIX (CNPJ):</p>
                <p className="text-white text-xl font-mono font-bold">
                  10.956.143/0001-25
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* DADOS DO PAGAMENTO */}
      <section className="py-8 bg-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="max-w-2xl mx-auto">
            <div className="bg-goodcard-gray rounded-lg p-6">
              <p className="text-sm text-goodcard-navy/70 mb-2">Dados que aparecerão no PIX:</p>
              <div className="space-y-1 text-sm text-goodcard-navy">
                <p><span className="font-semibold">Nome:</span> GOOD CARD</p>
                <p><span className="font-semibold">CNPJ:</span> 10.956.143/0001-25</p>
                <p><span className="font-semibold">Instituição:</span> Itaú Unibanco S.A.</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* RODAPÉ */}
      <footer className="py-6 bg-goodcard-navy">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <p className="text-center text-white/80 text-sm">
            GoodCard © 2026 - Cartão de Crédito para Combustível
          </p>
        </div>
      </footer>
    </div>
  )
}

export default App
