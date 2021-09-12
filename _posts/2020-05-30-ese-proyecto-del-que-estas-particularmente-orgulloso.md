---
layout: post
title:  Ese proyecto del que estás particularmente orgulloso
description: Porque los resultados fueron muy buenos, porque el equipo hizo piña con negocio...
date:   2020-05-30 19:00:00 +0100
image:  '/images/foto-navidad-2018-equipo-lowi.jpg'
tags:   []
---
> Para hacer desarrollo software ágil es imprescindible implementar buenas prácticas de desarrrollo, más allá de cualquier marco.

Me incorporé a al equipo Lowi en noviembre de 2017 y he estado en el mismo hasta mayo de 2020, con un rol híbrido entre Nexus Scrum Master y Software Develoment Manager. Sin ninguna duda, ha sido mi etapa profesinal más enriquecedora hasta la fecha y, también, la más dificil. Que ambas cosas hayan coincidido tampoco me sorprende, son los grandes retos los que más nos hacen crecer, aunque haya algunos tropiezos en el camino.

Lowi es la marca low-cost de Vodafone. Nació en 2014, solo con tres meses de desarrollo software el proyecto salió a producción y los clientes podían comprar una única línea móvil. Durante los 2.5 años que estuve en el equipo el número de clientes (suscripciones) creció de 270k a 1.5m. Sobra decir que este éxito es fruto del trabajo de muchas personas, pero me gustaría resaltar el trabajo del equipo de desarrollo de Paradigma Digital.

### Marco ágil y buenas prácticas de desarrollo

El equipo es responable tanto de la web pública, el área privada de clientes, el backoffice de marketing, el backoffice del call center, el portal de resellers, las aplicaciones móviles y el sistema de reporting. Partimos del marco de escalado ágil [Nexus](https://www.scrum.org/resources/online-nexus-guide) de [Scrum.org](https://www.scrum.org) y lo hemos adaptado a nuestras necesidades, prestando especial atención a la integración continua y a la gestión de dependencias cruzadas.

Asimismo, creamos unas convenciones internas con buenas prácticas (basadas en XP), estandarización del código, gobiernos de microservicios y apis,... que permiten que prácticamente cualquier desarrollador (~50) contribuyera en cualquier aplicación (frontend, backend), siempre que cumpliera las normas que nos otorgamos y que revisamos con frecuencia.

Para hacer desarrollo software ágil es imprescindible implementar buenas prácticas de desarrrollo, más allá de cualquier marco. Viene bien recordar uno de los principios del manifiesto ágil: "Continuous attention to technical excellence and good design enhances agility."

![Lowi Home]({{site.baseurl}}/images/lowi-es-completa.jpg)
*Pantallazo de la home de Lowi.es*

Uno de los grandes retos que tuvimos que enfrentarnos fue transformar un proceso de compra síncrono en asíncrono, de modo que si el flujo de compra se interrumpía en el algún punto del proceso (aprovisionamiento de SIM, alta en SAP, logística, etc.), la compra se reanudara automáticamente una vez la incidencia estuviera resuelta y el proceso de compra progresara.

Para ello, implementamos una arquitectura EDA (Event Driven Architecture), rompimos nuestro monolito de backend en microservicios (BaaS, DaaS) sobre EKS, usamos el patrón Productor/Consumidor, un sistema de colas con Kafka, y dedicamos muchas horas de trabajo y esfuerzo a aislar los distintos procesos y separar lógicas de negocio.

El resultado fue que cualquier caída de cualquier sistema dentro del proceso de compra (con muchas integracones con terceros) era totalmente transparente para el usuario, de modo que no se perdían compras, además de la consiguiente mejora en el servicio percibido por el usuario, la reducción de estrés por parte del equipo de soporte y la reducción de coste por llamadas a call center.
