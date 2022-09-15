---
title: source
slug: Web/HTML/Element/Source
translation_of: Web/HTML/Element/source
---
## Sumário

O elemento `source` é utilizado para especificar múltiplos recursos de mídia de elementos {{HTMLElement("picture")}}, {{HTMLElement("audio")}} ou {{HTMLElement("video")}} em HTML5. É um elemento vazio. É normalmente usado para disponibilizar [multiple formats supported by different browsers](/En/Media_formats_supported_by_the_audio_and_video_elements "En/Media formats supported by the audio and video elements").

## Contexto de uso

| Conteúdo permitido        | Nenhum; isso é um elemento vazio.                                                                                |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Omissão de tag            | Deve ter uma tag de início, mas não deve ter uma tag de fim.                                                     |
| Elementos pais permitidos | {{HTMLElement("picture")}}, {{ HTMLElement("audio") }}, {{ HTMLElement("video") }} |
| Documento normativo       | [HTML5, section 4.8.8](http://www.w3.org/TR/html5/video.html#the-source-element)                                 |

## Atributos

Como todos os outros elementos de HTML, esse elemento suporta os [global attributes](/en/HTML/Global_attributes "en/HTML/Global attributes").

- {{ htmlattrdef("src") }}
  - : Requerido, endereço do arquivo de mídia.
- {{ htmlattrdef("type") }}
  - : O tipo MIME do arquivo, opcionalmente com um parametro de `codecs`. Veja o [RFC 4281](http://www.rfc-editor.org/rfc/rfc4281.txt) para informações sobre como especificar codec.
- {{ htmlattrdef("media") }}
  - : Definição do tipo de mídia ([Media query](/en/CSS/Media_queries "En/CSS/Media queries")) pretendido.

Se o atributo **type** não está especificado, o tipo da mídia é obtido no servidor e é verificado se o Gecko consegue reproduzi-lo; se não for possível reproduzi-lo, o próximo **source** é verificado. Se o atributo **type** está definido, ele é comparado aos tipos que o Gecko consegue reproduzir, e se não for reconhecido, o servido não é solicitado; ao invés disso, o próximo elemento **source** é verificado.

## Interface do DOM

Esse elemento implementa a interface [`HTMLSourceElement`](/en/DOM/HTMLSourceElement "en/DOM/HTMLSourceElement").

## Exemplos

Esse exemplo demonstra como oferecer um vídeo no formato Ogg para usuários em que os navegadores suporta o formato Ogg, e um formato QuickTime para os usuários que o suporta. Se os elementos `audio` ou `video` não forem suportados pelo navegador, um aviso será mostrado. Se o navegador suportar o elemento, mas não suportar nenhum dos formatos especificados, um evento de `error` será lançado e os controles padrões de mídia (se ativados) indicarão o erro. Veja também a lista de [media formats supported by the audio and video elements](/En/Media_formats_supported_by_the_audio_and_video_elements "En/Media formats supported by the audio and video elements") em vários navegadores.

```html
<video controls>
  <source src="foo.ogg" type="video/ogg"> <!-- Escolhido pelo Firefox -->
  <source src="foo.mov" type="video/quicktime"> <!-- Escolhido pelo Safari -->
  Desculpa; seu navegador não é compatível com vídeo em HTML5.
</video>
```

Para mais exemplos, veja [Using audio and video in Firefox](/en/Using_HTML5_audio_and_video "En/Using audio and video in Firefox").

## Compatibilidade com navegadores

{{Compat("html.elements.source")}}