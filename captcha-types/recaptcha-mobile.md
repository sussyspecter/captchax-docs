---
markdown:
    toc:
        depth: 2
---
{% partial
    file="/_partials/captcha-types-template.md"
    variables={
        display_name: "reCAPTCHA Mobile",
        code_name: "ReCaptchaMobile",
        params_details: [
            {
                parameter: "pageAction",
                type: "String",
                required: "No",
                description: "Widget action value. Website owner defines what user is doing on the page through this parameter.",
            },
            {
                parameter: "isInvisible",
                type: "Boolean",
                required: "No",
                description: "Whether the ReCaptcha is invisible. Defaults to false.",
            },
        ],
        params_example: "{\n        \"websiteURL\": \"https://www.google.com/recaptcha/api2/demo\",\n        \"websiteKey\": \"6Le-wvkSAAAAAPBMRTvw0Q4Muexq9bi0DJwx_mJ-\",\n        \"pageAction\": \"login\",\n        \"isInvisible\": true\n    }",
         token: "03AFcWeA7vQiFmaYZWoYWht..."
    }
/%}
