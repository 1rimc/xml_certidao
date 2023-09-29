# Formato das Certidões em XML

Este documento fornece informações sobre o formato das certidões em XML utilizadas no projeto.

## Estrutura Básica

As certidões em XML seguem uma estrutura básica definida pelos esquemas (XSD) presentes na pasta `esquemas/`. A estrutura geral inclui os seguintes elementos:

- `<CERTIDAO>`: Elemento raiz que contém as informações principais da certidão.
- `<IMOVEIS>`: Elemento que inclui informações sobre os imoveis.
- `<ATOS>`: Elemento que inclui informações sobre os atos praticados.


## Exemplo de Certidão em XML

Aqui está um exemplo simplificado de uma certidão em XML:

```xml
<CERTIDAO>
  <NUMERO_PEDIDO>10000</NUMERO_PEDIDO>
  <NUMERO_REGISTRO>50000</NUMERO_REGISTRO>
  <LIVRO>2</LIVRO>
  <CNM>2</CNM>
  <DATA_REGISTRO>1990-05-04</DATA_REGISTRO>
  <IMOVEIS>
    <IMOVEL>
      <URBANO>
        <LOTE>2</LOTE>
        <QUADRA>5</QUADRA>
        <IPTU/>
        <IM/>
        <AREA_PRIVATIVA_PRINCIPAL/>
        <AREA_PRIVATIVA_ACESSORIA/>
        <AREA_PRIVATIVA_TOTAL/>
        <AREA_USO_COMUM/>
        <AREA_TOTAL/>
        <AREA_USO_COMUM_TERRENO/>
        <AREA_USO_EXCLUSIVO_TERRENO/>
        <AREA_TOTAL_TERRENO/>
        <FRACAO_IDEAL/>
        <AREA_IMOVEL>50.0</AREA_IMOVEL>
      </URBANO>
      <RURAL>
        <DENOMINACAO></DENOMINACAO>
        <AREA></AREA>
        <CIR></CIR>
        <CCIR></CCIR>
        <NIRF></NIRF>
        <CAR></CAR>
      </RURAL>
    </IMOVEL>
  </IMOVEIS>
  <ATOS>
    <ATO>
      <NUMERO_ATO>1</NUMERO_ATO>
      <DATA_ATO>2023-06-01</DATA_ATO>
      <DENOMINACAO>Averbacao</DENOMINACAO>
      <PARTES/>
    </ATO>
    <ATO>
      <NUMERO_ATO>2</NUMERO_ATO>
      <DATA_ATO>2023-07-01</DATA_ATO>
      <DENOMINACAO>Compra e Venda</DENOMINACAO>
      <PARTES>
        <PARTE>
          <QUALIFICACAO>transmitente</QUALIFICACAO>
          <PERCENTUAL>100.0</PERCENTUAL>
          <PESSOA_FISICA>
            <NOME>NOME PESSOA</NOME>
            <CPF>00000000000</CPF>
          </PESSOA_FISICA>
          <PESSOA_JURIDICA/>
        </PARTE>
        <PARTE>
          <QUALIFICACAO>adquirente</QUALIFICACAO>
          <PERCENTUAL>100.0</PERCENTUAL>
          <PESSOA_FISICA>
            <NOME>NOME PESSOA</NOME>
            <CPF>00000000000</CPF>
          </PESSOA_FISICA>
          <PESSOA_JURIDICA/>
        </PARTE>
      </PARTES>
    </ATO>  
  </ATOS>
</CERTIDAO>