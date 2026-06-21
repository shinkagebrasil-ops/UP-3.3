# SHIN KAGE CRIPTO v2 - Pacote PWA Tático

**Versão de Combate Revisada e Padronizada**

## O que foi corrigido
- Erro crítico de nomenclatura singular (`conn`, `currentCall`) que quebrava suporte a múltiplos operadores.
- Agora suporta múltiplos operadores com broadcasting de status (quem está falando, quem entrou).
- Host (Líder/TOC) ouve todos os operadores simultaneamente.
- Operadores ouvem o host.
- PTT floor control visível em tempo real para toda a equipe.
- Service Worker atualizado para cachear o beep Nextel.
- Nomenclatura padronizada com prefixo `sk_`.
- Topologia estrela otimizada para operações de equipe pequena (2-6 operadores).

## Como usar (Deploy Rápido)

1. **Coloque o arquivo de áudio**  
   Copie `alerta-beep-nextel-e139.mp3` (o mesmo do seu original) para dentro desta pasta.

2. **Hospedagem recomendada (tática)**
   - GitHub Pages (gratuito e rápido)
   - Cloudflare Pages
   - Netlify
   - Ou servidor próprio com HTTPS (obrigatório para WebRTC e getUserMedia)

3. **Instalação no celular**
   - Abra o site no Chrome/Safari
   - Toque em "Instalar no Celular"
   - Aceite → vira app nativo com ícone

4. **Uso em operação**
   - Um operador cria o canal (vira Host/Líder)
   - Compartilha o código de 4 dígitos
   - Demais operadores entram com o código
   - Todos veem quem está no canal e quem está transmitindo
   - PTT funciona com toque longo ou tecla Espaço (desktop)

## Limitações conhecidas (honestas)
- Voz: Host ouve todos. Operadores ouvem apenas o Host (topologia estrela).
- Para voz full-mesh entre todos os operadores simultaneamente, seria necessário SFU (mediasoup/Jitsi custom) ou full mesh signaling — mais pesado.
- Modo Pós-Quântico é apenas UI por enquanto (WebRTC nativo já é muito forte).

## Próximos passos sugeridos (se precisar)
- Integração com servidor de signaling próprio (para evitar peerjs.com cloud)
- SFU para voz full group
- QR Code para join rápido sem digitar código
- Criptografia adicional de metadados

**Pronto para campo. Sem travas. Máxima potência.**

Shin Kage — 2026