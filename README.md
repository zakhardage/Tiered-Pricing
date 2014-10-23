Tiered-Pricing
==============

Step 1. Update product.liquid

Find <form action="/cart/add" method="post"> ... </form>
Wrap this in the following conditional liquid statement:
{% if product.options[0] == 'Rate' or product.options[0] == 'rate' %}
	{% include 'tiered-pricing' %}
{% else %}
	<form action="/cart/add" method="post"> ... </form>
{% endif %}


Step 2. Upload the tiered-pricing.liquid file to the snippets folder



Step 3. Add tiered pricing rates to your product listing

Change the first product option title to "Rate"
Enter variants/rates in increasing value and use only numbers (e.g. 1, 5, 10, 20, 50)