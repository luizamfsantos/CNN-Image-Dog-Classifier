# Pet Image Classification using Pretrained CNN Models

This repository contains a Python program for classifying pet images using pretrained CNN (Convolutional Neural Network) models. The program compares the classifications with the true identity of the pets in the images and summarizes the CNN's performance on the classification task. It evaluates three different CNN model architectures to determine the most effective one for classification.

## Program Overview

The main program, `check_images.py`, orchestrates the entire classification process. It involves several modules and functions:

- `get_input_args.py`: Retrieves command-line arguments from the user, such as the directory with images, the chosen model architecture, and the file containing dog names.
- `get_pet_labels.py`: Extracts pet image labels from filenames and creates a results dictionary.
- `classify_images.py`: Utilizes the pretrained CNN model to classify images and updates the results dictionary with classifier labels.
- `adjust_results4_isadog.py`: Adjusts the results to identify if the classifier correctly identified images as 'a dog' or 'not a dog'.
- `calculates_results_stats.py`: Computes result statistics, including counts and percentages, and generates a summary in a results statistics dictionary.
- `print_results.py`: Prints a summary of results, including incorrectly classified dogs and breeds if requested.

## Usage

To execute the program, use the following command-line arguments:

```bash
python check_images.py --dir <directory with images> --arch <model> --dogfile <file that contains dog names>
```

- `--dir`: Specifies the directory containing pet images.
- `--arch`: Chooses the CNN model architecture among the available options.
- `--dogfile`: Provides the file containing a list of dog names.

Example:

```bash
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt
```

## Instructions for Running

1. Ensure you have Python 3 installed on your system.
2. Clone this repository.
3. Install the necessary dependencies (if any) by referring to the `requirements.txt` file.
4. Run the program by executing `check_images.py` with appropriate command-line arguments as described above.

## Additional Notes

- The program measures and displays the total elapsed runtime upon completion.
- Feel free to modify or extend the code to suit your specific needs.
