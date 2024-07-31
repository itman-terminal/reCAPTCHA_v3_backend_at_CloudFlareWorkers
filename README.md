# reCAPTCHA_v3_backend_at_CloudFlareWorkers



A backend for reCAPTCHA v3 run on CloudFlare Workers
-Demo site:https://itman-terminal-github-io.pages.dev/h
-Serverless operation

-Modifiable range of back-end request sources

-Host on <a href=https://workers.dev>Cloudflare Workers</a>

**Cloudflare Workers' domain https://workers.dev is blocked in mainland China, so the backend needs to bind to an unblocked domain name**

<h1>Prepare</h1>

<h2>workers.js</h2>
Open workers.js in a text editor, search for
`Your_Secret_key_here` and replace it with your SecretKey

(Visit [https://www.google.com/recaptcha/admin](https://www.google.com/recaptcha/admin)to view your SiteKey and SecretKey).Finally, you just need to deploy the js file to Cloudflare Workers

Tips:you can edit `'Access-Control-Allow-Origin': '*',`replace.`*`as your website(Example:`'Access-Control-Allow-Origin': 'https://github.com',`)

<h2>index.html</h2>
-You need to download index.html and workers.js , use a text editor to open index.html, search for

`Your_site_key_here`
in index.html, and replace your own reCAPTCHA SiteKey.（Note: There are 2 places that need to be replaced.）
Next,search
`https://your.workers.backendyour.workers.backend/verify` and replace it with your Workers backend(Example:`https://recaptchabackend.yourname.workers.dev/verify`).Then you just need to upload.the html to you website.
