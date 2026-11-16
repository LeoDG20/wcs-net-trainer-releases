<p align="center">
  <img src="assets/banner.png" alt="WCS-Net Trainer" width="100%">
</p>

<p align="center">
  <a href="https://github.com/LeoDG20/wcs-net-trainer-releases/releases/latest"><img alt="Versão" src="https://img.shields.io/github/v/release/LeoDG20/wcs-net-trainer-releases?label=vers%C3%A3o&color=8B5CF6&style=flat-square"></a>
  <a href="https://github.com/LeoDG20/wcs-net-trainer-releases/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/LeoDG20/wcs-net-trainer-releases/total?label=downloads&color=8B5CF6&style=flat-square"></a>
  <img alt="Windows 10 e 11" src="https://img.shields.io/badge/Windows-10%20%7C%2011-1f2937?style=flat-square">
  <img alt="Assinatura Ed25519" src="https://img.shields.io/badge/atualiza%C3%A7%C3%A3o-assinada%20Ed25519-1f2937?style=flat-square">
</p>

<p align="center">
  <a href="https://github.com/LeoDG20/wcs-net-trainer-releases/releases/latest"><b>⬇&nbsp; Baixar a versão mais recente</b></a>
</p>

Treina as **redes neurais** do [Whisper Corpus Studio](https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest). O WCS cuida da curadoria e exporta o dataset; o Trainer treina e devolve um *model pack* assinado, que o WCS importa.

## Recursos

- **Importa o dataset do WCS:** o contrato é versionado, e o que não confere com ele é recusado, não adivinhado.
- **Treino com acompanhamento:** progresso, tempo, métricas e matriz de confusão do conjunto de avaliação.
- **Model pack assinado:** exporta a rede com assinatura Ed25519; o WCS só aceita pacotes verificados.
- **Independente do WCS:** pode rodar em outra máquina, sem o stack de áudio nem a interface de curadoria.

## Instalação

1. Em [Releases](https://github.com/LeoDG20/wcs-net-trainer-releases/releases/latest), baixe **`WCS-Net-Trainer-Setup-<versão>.exe`**.
2. Execute o instalador. Requer Windows 10 ou 11 (64 bits); não precisa de administrador.
3. Se aparecer *“O Windows protegeu o computador”*, clique em **Mais informações → Executar assim mesmo** (veja a pergunta abaixo).

## Atualização automática e segurança

O programa instalado verifica este repositório e se atualiza sozinho, baixando apenas o que mudou. Antes de aplicar qualquer arquivo ele confere a **assinatura Ed25519** contra a chave pública embutida nele; arquivo sem assinatura válida é recusado. A chave privada fica apenas com o autor e nunca é publicada.

## Perguntas frequentes

<details>
<summary><b>Por que o Windows mostra um aviso ao instalar?</b></summary>

O instalador não usa certificado comercial de editor, então o SmartScreen avisa para qualquer programa novo. A autenticidade é garantida pela assinatura Ed25519 descrita acima. Clique em **Mais informações → Executar assim mesmo**.

</details>

<details>
<summary><b>Preciso do WCS instalado?</b></summary>

Para gerar o dataset, sim. O Trainer em si só precisa do dataset exportado.

</details>

<details>
<summary><b>Como desinstalo?</b></summary>

Em **Configurações do Windows → Aplicativos → Aplicativos instalados**.

</details>

<details>
<summary><b>Para que servem os outros arquivos de cada release?</b></summary>

Só o instalador (`Setup.exe`) interessa a quem instala. `manifest.json`, `package.zip`, `patch.zip` e os arquivos `.sig` são usados pela atualização automática e pela verificação de assinatura.

</details>

## Programas da família

| Programa | Função | Download |
| --- | --- | --- |
| Whisper Corpus Studio | Curadoria do corpus: segmentar, revisar e exportar o dataset. | [Baixar](https://github.com/LeoDG20/whisper-corpus-studio-releases/releases/latest) |
| **WCS-Net Trainer** | Treino das redes neurais a partir do dataset exportado pelo WCS. | [Baixar](https://github.com/LeoDG20/wcs-net-trainer-releases/releases/latest) |
| WCS Gold Set | Concordância entre versões de segmentação (você, orientador, colegas). | [Baixar](https://github.com/LeoDG20/wcs-gold-set-releases/releases/latest) |

---

<sub>Repositório de distribuição: o código-fonte é privado. Dúvidas ou problemas: abra uma <a href="https://github.com/LeoDG20/wcs-net-trainer-releases/issues">issue</a>.<br>
© 2026 Leo Gobbi · uso acadêmico (TCC/IC).</sub>
