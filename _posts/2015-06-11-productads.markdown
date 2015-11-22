---
layout: nav
title:  "Product Ads "
---

<h6>Product Ads</h6>

Product Advertising is a method of communicating or broadcasting the promotion of a product to persuade a customer to purchase the product. A good advertisement can educate the customer with the benefits derived from its use. The idea is to increase the brand awareness and seek customer attention to buy a particular product.

<h6>How to integrate Product Ads in the Snapdeal  webpage</h6> 
The Following API will return information about a Creative of the Product Ad. 

<strong>API Link: [Product Ads API]({% post_url 2015-06-11-productapi %})</strong>

	<iframe src="http://52.5.245.198:9009/pub/getAd?pubId=1&js=true&siteId=101&impressionId=hello&similar_ads=false&inv=site&category=
	MOBILES&adspaceId=1006&pagetype=category&rs=html">
	</iframe>
The above tag should be integrated with the publisher webpage to get a product or Banner ad.

<strong>Example</strong>

	<html>
	<body>
	<iframe src="http://52.5.245.198:9009/pub/getAd?pubId=1&js=true&siteId=101&impressionId=hello&similar_ads=false&inv=site&category=MOB
	egory&rs=html">
	<p>Your browser does not support iframes.</p>
	</iframe>
	</body>
	</html>

<strong>Sample Result</strong>

<img src="{{ site.baseurl }}/img/productadnew.png">