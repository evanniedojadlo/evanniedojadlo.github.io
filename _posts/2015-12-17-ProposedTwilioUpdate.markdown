---
layout: post
title:  "Twilio Wishlist"
date:   2015-12-17 19:18:16
categories: Twilio, Ruby
---

I wish that it was possible to append pre-hosted voice attributes on Twilio verbs "out of the box", specifically the "allowed value" Jar-Jar Binks from the Star Wars universe. Just imagine how ecstatic your customers will be to receive a voice prompt from the most beloved character of the series.

Twilio verb example with proposed voice values:

	<?xml> version="1.0" encoding="UTF-8"?>
	<Response>
			<Gather timeout="10" finishOnKey="*">
				<Say voice="JarJarBinks">Please enter your pin number and then press star.</Say>
			</Gather>
	</Response>

Other notable favorites:
	<Say voice="CableGuy">Please enter your pin number and then press star.</Say>

	<Say voice="Gottfried">Please enter your pin number and then press star.</Say>

Current documentation which shows the two current voice engines :) [https://www.twilio.com/docs/api/twiml/say]{:target="_blank"}

