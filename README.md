# wordpres{

"$schema": "https://playground.wordpress.net/blueprint-schema.json",
"preferredVersions": {
"php": "8.3",
"wp": "latest"
},
"features": {
"networking": true
},
"login": true,
"landingPage": "/",
"siteOptions": {
"blogname": "{{sitename}}",
"permalink_structure": "/%postname%/",
"timezone_string": "{{timezone}}"
},
"constants": {
"WP_DEBUG": false
},
"steps": [
{
"step": "installTheme",
"themeData": {
"resource": "url",
"url": "https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/themes/kadence.zip"
},
"options": {
"activate": true
}
},
{
"step": "installPlugin",
"pluginData": {
"resource": "url",
"url": "https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/plugins/kadence-blocks.zip"
},
"options": {
"activate": true
}
},
{
"step": "installPlugin",
"pluginData": {
"resource": "url",
"url": "https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/plugins/advanced-custom-fields.zip"
},
"options": {
"activate": true
}
},
{
"step": "installPlugin",
"pluginData": {
"resource": "url",
"url": "https://raw.githubusercontent.com/ehsanmoattari/wordpress-portfolio/main/plugins/bookingpress.zip"
},
"options": {
"activate": true
}
},
{
"step": "importWxr",
"file": {
"resource": "url",
"url": "{{content_url}}"
}
}
]
}s-portfolio
