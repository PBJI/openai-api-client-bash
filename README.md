### Bash Script Help Manual: OpenAI API Request
# Introduction

This bash script is designed to interact with the OpenAI API and make requests for text generation. The script takes in various command line arguments and options, prompts the user for input, and saves the generated text to a file along with a timestamp.
Command Line Arguments

### Global Environment Variable

Before one use this script, it is reconmmended to set the OPENAI_API_KEY=$API_KEY in the environment variable. This will ensure the script regardless of any explicit methods of providing the API KEY to the program. Remember the environment variable name should be OPENAI_API_KEY and its value should be the API KEY without any other special characters.

### The script takes the following command line arguments:

-k [API_KEY] : Sets the OpenAI API key to use for making requests. This argument is optional, but if not provided, the script will attempt to retrieve the key from the bash profile or global environment variables.

-g : Sets the script to use the API key saved globally in the bash profile.

-o [OUTPUT_FILE] : Sets the output file to which the generated text will be saved. The default value is "response.txt".

-m [MODEL] : Sets the OpenAI model to use for text generation. The default value is "text-davinci-002".

-t [TEMPERATURE] : Sets the temperature value for text generation. The default value is 0.7.

-x [MAX_TOKENS] : Sets the maximum number of tokens to generate in the generated text. The default value is 1500.

-p [TOP_P] : Sets the top-p value for text generation. The default value is 1.

-f [FREQUENCY_PENALTY] : Sets the frequency penalty value for text generation. The default value is 0.

-r [PRESENCE_PENALTY] : Sets the presence penalty value for text generation. The default value is 0.
Usage

### To use the script, run it from the command line with the desired command line arguments and options. For example:

Give the script "davinci" executable permission and move it to bin folder.

davinci -k [API_KEY] -o [OUTPUT_FILE] -m [MODEL] -t [TEMPERATURE] -x [MAX_TOKENS] -p [TOP_P] -f [FREQUENCY_PENALTY] -r [PRESENCE_PENALTY]

After running the script, the user will be prompted to enter text input. The generated text will then be saved to the specified output file with a timestamp.

# Error Handling

The script will exit with an error message if the API key is not provided and cannot be retrieved from the bash profile or global environment variables.

If an invalid command line argument is provided, the script will display an error message and exit.

If an option requires an argument, but no argument is provided, the script will display an error message and exit.

# Notes

The script uses the "jq" command to parse the API response and extract the generated text. If "jq" is not installed on your system, the script will not work properly.
