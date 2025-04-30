Travel Planner 

The goal of this project is to use OpenAI GPT-3 Chat completion to generate a travel itinerary for a user. The user will be able to specify a destination, a trip duration, budget and more. The user will also be able to specify a few activities they would like to do. The Travel Planner will then generate a travel itinerary for the user.



## Getting Started
After cloning the backend from Altogic Marketplace, you can rename .env.example to .env and add your REACT_APP_ENDPOINT_URL to the .env file.
## How to use 
1. Clone the repo

2. Install the dependencies

3. Run the app Go to http://localhost:3000/

## How it works
The app uses OpenAI's GPT-3 API with Altogic Integration to generate the travel itinerary. The app is built using Altogic and React. If you want to learn more about Altogic, check out the [Altogic Documentation](https://agnost.dev/)

## How to integrate with OpenAI
1. Create an account on OpenAI

2. Create an API key

3. Create an account on Altogic

4. Create a new project

5. Create a new endpoint and service with POST method and travel as the endpoint path.

6. Open the service design and click the Start node, and define Request Body to Custom Model and click Add Field and select prompt as the field name.

7. Click the Marketplace tab and search for OpenAI Chat Completion and move it to the design area.

8. Click the OpenAI Chat Completion node and fill the prompt with following code:

```[
  {
    "role": "user",
    "content": {{CONCAT(input.body.prompt, "Format your response using Markdown. Use headings, subheadings, bullet points, and bold to organize the information.")}}
  }
]

9. Define the API Key field with your OpenAI API key.

10. Connect the Start node to the OpenAI Chat Completion node.

11. Find the Return Success Response node and move it to the design area. Connect the OpenAI Chat Completion node to the Return Success Response node.

12. Copy the endpoint URL and paste it in the .env file. The .env file should look like this:REACT_APP_ENDPOINT_URL =
    "https://c3-na.altogic.com/e:6427519d2f0b61e4d9dda50f/travel";

    



