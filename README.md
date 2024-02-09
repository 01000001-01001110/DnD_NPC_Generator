# DnD NPC Generator Documentation

This Python script provides functionality for generating fictional characters with various attributes such as name, gender, race, and more. The script consists of several functions, each serving a specific purpose in the character creation process.

## Functions

### `generate_character(genders, race_details)`

Generates a single character with attributes based on the input parameters.

- **Parameters:**
  - `genders`: A list of genders to choose from.
  - `race_details`: A dictionary containing details for each race, including names, archetypes, backgrounds, physical characteristics, alignment, culture, and lore.
- **Returns:** A dictionary representing a character with randomly selected attributes.

### `generate_characters_list(n, genders, race_details)`

Generates a list of characters.

- **Parameters:**
  - `n`: The number of characters to generate.
  - `genders`: A list of genders to choose from.
  - `race_details`: A dictionary containing detailed attributes for character generation.
- **Returns:** A JSON string representing a list of generated characters, formatted with an indentation of 4 spaces.

### `save_characters_to_file(characters_json)`

Saves the generated characters to a JSON file.

- **Parameters:**
  - `characters_json`: A JSON string of generated characters.
- **Behavior:** The function saves the characters to a file named with the format `{number_of_characters}_characters_{current_date}.json` and prints a message indicating the save operation's success.

### `main()`

Main function to run the character generator script. It prompts the user for the number of characters to generate, generates them, and saves them to a file.

### `validate_race_details(race_details)`

Validates the `race_details` data structure to ensure it meets the expected format, especially for height and weight ranges.

- **Parameters:**
  - `race_details`: A dictionary containing detailed attributes for character generation.
- **Behavior:** Prints error messages for any discrepancies found in the height and weight ranges for each gender within each race.

## Usage

To use the script, ensure that you have defined the `genders` and `race_details` according to the expected format and then run the script. If necessary, use `validate_race_details(race_details)` to check your data structure for errors before generating characters.

Note: This script uses the `random` module for attribute selection and `json` module for JSON handling, so make sure these are imported at the beginning of your script.
