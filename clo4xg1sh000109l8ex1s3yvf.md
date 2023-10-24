---
title: "Cloudflare y el temible ERR_TOO_MANY_REDIRECTS 😱"
seoDescription: "Solucionar ERR_TOO_MANY_REDIRECTS de Cloudflare."
datePublished: Tue Oct 24 2023 22:57:42 GMT+0000 (Coordinated Universal Time)
cuid: clo4xg1sh000109l8ex1s3yvf
slug: cloudflare-y-el-temible-errtoomanyredirects
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1698188142632/d0d18433-3367-415b-aad7-347f6a057497.png
tags: cloudflare, ssl, hosting, google-domains, errtoomanyredirects

---

Me doy la libertad de escribir este artículo para compartir una solución a un problema muy simple, pero también como recordatorio para mí mismo en caso de futuras incidencias 😇.

Google vendió su apartado de Google Domains a Squarespace, y yo, claro, tenía un dominio ahí. Cuando lo trasladé de Google a Cloudflare (ya tenía mi dominio usando los servicios de Cloudflare para el SSL y otras herramientas de seguridad, por lo tanto no fue necesaria ninguna configuración adicional de los DNS en el traslado de un registrador a otro), a las horas me llamaron y me comentaron que el sitio estaba caído 😨 y yo dijé omaiga! jaja.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698187886735/94238c96-3baa-43d1-bce7-294f735e8242.png align="center")

El error que recibí fue ERR\_TOO\_MANY\_REDIRECTS. Me puse a documentarme del tema, hay un artículo muy completo de [Cloudflare al respecto](https://developers.cloudflare.com/ssl/troubleshooting/too-many-redirects/). Revisé cada regla, firewall y configuración que posiblemente fuera errónea, pero finalmente encontré la solución en un video de [YouTube](https://www.youtube.com/watch?v=QIDQVsETwfA), y escribo esto por que personalmente prefiero leer, pero están invitados a ver el video si lo desean 😁.

\-- La solución es muy simple. Si no quieren leer todo lo anterior 😆, sepan que el modo de encriptación Desactivado y Flexible producen el error. Para solucionarlo, solo deben elegir el modo Completo o Estricto (Full).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698187343217/7445aec4-6eb8-43ff-9fae-b2f968678f36.png align="center")

Espero que a alguien le sea de utilidad y no demoren mucho con sus sitios caidos por estas sorpresas que nos da Cloudflare jaja 😄