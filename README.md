# NLT API ChatGPT Action

This is a simple action that allows you to use the NLT API in ChatGPT.

## Usage

To use the action, you need to have an API key from NLT. You can get one by signing up for an account at https://nlt.to.

Once you have your API key, you can use the action in ChatGPT by following these steps:

1. Create or edit a Custom GPT in ChatGPT.
2. In the "Configure" tab, click the "Create new action" button in the Actions section.
3. Copy the contents of `nlt-api-gpt-action-schema.yml` into the action configuration (Schema).
    * OR, you can paste the [URL to the raw file](https://raw.githubusercontent.com/jtsternberg/NLT-API-Custom-GPT-Action/master/nlt-api-gpt-action-schema.yml) into the "Immport from URL" field.
4. Replace the `<apikey>` in the Schema with your API key. (you can get this [from them](https://api.nlt.to/))
5. Leave the "Authentication" setting at "None".
6. See that two Available Actions are now shown.
7. Click the "Test" button next to the `GetPassages` action.
8. Verify that the chat tests the api and generates a response with the sample reference (Romans 8:28-30).
9. Click the "Create" or "Update" button to save the Custom GPT.
10. You can now use the action in your Custom GPT conversations.

