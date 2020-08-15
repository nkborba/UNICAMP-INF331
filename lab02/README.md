# Lab 02
## Aluno: Nicholas Borba

### Tarefa sobre catálogo de componentes

### Web Components 1
~~~HTML
<dcc-trigger label="Mundo" action="message/mundo/politica" value="Política Mundial"></dcc-trigger>
<dcc-trigger label="Brasil P" action="message/brasil/politica" value="Política Nacional"></dcc-trigger>
<dcc-trigger label="Brasil E" action="message/brasil/esporte" value="Esportes Brasil"></dcc-trigger>
<dcc-trigger label="Bahia" action="message/bahia/esporte" value="Bahia Esporte"></dcc-trigger>

<dcc-lively-talk duration="0" character="doctor" speech="Veja isso: ">
    <subscribe-dcc topic="message/+/politica"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk duration="0" character="nurse" speech="E isso também é importante: ">
    <subscribe-dcc topic="message/brasil/#"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk duration="0" character="patient" speech="Mas você já viu essa de ">
    <subscribe-dcc topic="message/#"></subscribe-dcc>
</dcc-lively-talk>
~~~

### Web Components 2
~~~HTML
<dcc-trigger label="Ver notícias" action="next/rss"></dcc-trigger>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/rss" role="step" ></subscribe-dcc>
</dcc-rss>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/rss" role="step" ></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk duration="0" character="doctor" speech="Aqui estarão as noticias agregadas de Ciências">
    <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk duration="0" character="nurse" speech="Aqui estará alguma notícia de Ciência">
    <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk duration="0" character="patient" speech="E aqui, alguma sobre Design">
    <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
~~~
