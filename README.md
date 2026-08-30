# Dog Breed Image Classifier

A Python application that uses pre-trained Convolutional Neural Networks (CNNs) to classify pet images, compare true labels against model predictions, and evaluate performance across different architectures (ResNet, VGG, and AlexNet).

## Project Overview
This project is part of the AI Programming with Python Nanodegree. It demonstrates fundamental computer vision pipeline concepts, command-line argument parsing with `argparse`, dictionary data structures in Python, and performance evaluation metrics.

## Key Features
- **Input Parsing:** Handles command-line arguments for image directory (`--dir`), model architecture (`--arch`), and dog name definitions (`--dogfile`).
- **Data Labeling:** Extracts true pet labels automatically from filenames.
- **Image Classification:** Leverages PyTorch-based pre-trained CNN models via a helper classifier interface.
- **Dog Verification:** Adjusts results to evaluate whether models correctly distinguish dogs from non-dog subjects.
- **Statistical Analysis:** Computes and summarizes classification counts, match percentages, and model runtime.

## Project Structure
- `check_images.py`: The main orchestrator script running the program flow.
- `get_input_args.py`: Handles parsing of command-line arguments.
- `get_pet_labels.py`: Extracts pet image labels from filenames.
- `classify_images.py`: Runs images through CNN models to generate predictions.
- `adjust_results4_isadog.py`: Compares classifier labels against standard dog name lists.
- `calculates_results_stats.py`: Computes statistics, counts, and percentages.
- `print_results.py`: Formats and displays final summary outputs.

## Example Usage
Run the script from your terminal specifying the image directory, CNN architecture, and dog reference file:
```bash
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt