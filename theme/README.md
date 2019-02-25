## STEP 1:
In templates/article.liquid, replace:
`
{{ article.content }}
`
with:
`
{% include 'shortcode' load: article.content %}
`

## STEP 2:
Add this CSS to theme.scss.liquid
`
/* Product shortcode in Blog articles */
.sc_product_wrapper {
  float: left;
}
.sc_product_image {
  width: auto;
  float: left;
  margin-right: 20px;
}
.sc_product_wrapper a, .sc_product_wrapper a:hover {
  text-decoration: none !important;
  border:0px;
}
.sc_product_link, sc_product_link:hover {
  padding:8px;
  background-color: #3333CC;
  color: #FFF !important;
  padding: 8px 16px 8px 16px;
  border-radius: 25px;
}
.sc_product_link:hover {
  background-color: #9999FF;
}
`

## STEP 3:
In the individual blog post text, insert the shortcodes where you want them to appear:
e.g.
https://mysite.myshopify.com/admin/blogs/22899720214/articles/26946568214
[single-product handle="arbois-cardigan" image_size="200x200" title="The Arbois Cardigan Pattern" description="This long, light, and gently shaped cardigan has deep pockets and a versatile collar." link_text="Check it out"]
[single-product handle="castellane-pullover"]

## STEP 4:
There is no step 4


# Shortcode functionality courtesy Culture Kings
https://github.com/culturekings/shopify-shortcodes
/theme/snippets/shortcode-render.liquid
/theme/snippets/shortcode.liquid
Both files used unaltered.
