# The AI-Powered API Builder: Instructions & Links

1. Open and copy the prompt from: https://github.com/paraskakis/apidesign/blob/main/Gemini2Prompt.md

2. Paste the prompt into Gemini 2.5 Pro (preview) and change the last line to reflect the API you're building: https://gemini.google.com/app

3. Copy the generated OpenAPI file and paste into Scalar Editor to check for issues. Save it to a JSON file: https://editor.scalar.com/

4. Upload the file into Rate My OpenAPI. You can improve the score taking the eimailed feedback and pasting back into Gemini: https://ratemyopenapi.com/

5. Get a second opinion OpenAPI Doctor https://pb33f.io/doctor

6. Once you get good results, uload the OpenAPI file into Mockbin to generate a prototype: https://mockbin.io/

7. Use HTTPie for testing: https://httpie.io/app

8. Sign up for Replit and upload the OpenAPI file: https://replit.com/

9. Open and paste the following prompt https://github.com/paraskakis/apidesign/blob/main/ReplitCode.md

10. Hit `Start Building` and review the plan by Replit Agent. Go simnple to start with and do not select persistence, logging or any other proposed additions.

11. Use the green link in the Preview pane link to test the generated API with HTTPie. Ask Replit for a demo API Key if it hasn;t offered it yet. Feed any errors or suggestions back to Replit Agent and let it correct them. If you get stuck go backa checkpoint, or start from scratch.

12. Sign up for Zuplo  (Start for Free): https://zuplo.com/

13. Create a new project and navigate to `Start Building | Code | routes.oas.json | OpenAPI`. Then hit `Import OpenAPI`: https://zuplo.com/

14. `Complete Merge`, `Save` and go to `Code | routes.oas.json | Route Designer`

15. Pick a route such as the GET collection and paste the Replit URL into `Forward to`. Continue with other routes - Don't forget to hit `Save`.

16. Exit the project and copy the Zuplo hosted URL for your gateway at the top left. Test the gateway with HTTPie by hitting this URL. Don't forget to add Authentication.

17. Go back into Zuplo and check Logging and Analytics!

## Additonal links:

A generated OpenAPI file, in case you run into any trouble: https://github.com/paraskakis/apidesign/blob/main/dad-jokes-api.json

A quick test sequence: https://github.com/paraskakis/apidesign/blob/main/TestSequence.md

API Product Mastery for Experienced PMs course with 20% discount: https://tinyurl.com/apipmapidays

Talk Slides: https://speakerdeck.com/paraskakis/the-ai-powered-api-builder-speeding-up-api-delivery-with-ai-tools

