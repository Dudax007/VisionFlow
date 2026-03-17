# VisionFlow

👁️ VisionFlow: Touchless UX & Privacy AIO VisionFlow é uma plataforma experimental de interface web desenvolvida para o projeto "AI Experience". O objetivo é redefinir a interação humano-computador (HCI) ao transformar a webcam em um sensor inteligente que entende gestos e intenções, garantindo acessibilidade e privacidade sem o uso de periféricos físicos.

💡 A SoluçãoO projeto resolve dois problemas principais de UX:Interação Sem Contato: Navegação fluida em telas onde o toque é indesejado (ex: ambientes médicos, quiosques públicos ou limitações motoras).Segurança de Dados: Proteção automática de informações sensíveis contra olhares curiosos em ambientes compartilhados.

🚀 Funcionalidades PrincipaisAir-Cursor Control: Controle do cursor do mouse através do rastreamento em tempo real do dedo indicador.Gestual Click: Reconhecimento do gesto de "pinça" (polegar + indicador) para acionar eventos de clique.Smart Privacy (Auto-Blur): Monitoramento do olhar (Gaze Tracking). Se o usuário desvia o olhar da tela, o CSS da página aplica instantaneamente um efeito de desfoque (blur).Interface Responsiva: Frontend adaptado para responder aos comandos enviados via backend em alta velocidade.

🛠️ Stack TecnológicaO projeto foi construído utilizando uma arquitetura que integra o processamento pesado de IA com a agilidade do desenvolvimento Web:CamadaTecnologiaFunçãoIA & CorePythonLinguagem base para processamento de dados.Computer VisionMediaPipeMapeamento de Landmarks das mãos e Face Mesh.Image ProcessingOpenCVCaptura e manipulação de frames de vídeo.InterfaceHTML5 / CSS3Estrutura e estilização da interface adaptativa.ComunicaçãoFlask-SocketIOProtocolo WebSocket para latência ultrabaixa.
