# Genre Recognition with Fast Fourier Transform
This code is a Python implementation for recognizing the genre of a song using the Fast Fourier Transform (FFT) algorithm in Colab. The algorithm works by dividing each song into segments and applying FFT to each segment. The resulting spectra are stored in a dictionary where each genre has a list of spectra of its songs.


## Usage
To use the algorithm, you can call the classify_song() function with the path to the song to classify as an argument. The function returns the most probable genre for the song.
```
genre = classify_song('path/to/song')
```
## Implementation
The implementation consists of two main parts:

1. Generating the Spectra Database
The first part reads each song from the dataset, divides it into segments, and applies FFT to each segment. The resulting spectra are stored in a dictionary where each genre has a list of spectra of its songs. The average spectrum of each genre is calculated, and the resulting spectra are stored in a second dictionary where each genre has its average spectrum.

2. Classifying a New Song
The second part of the implementation takes a new song as input, divides it into segments, applies FFT to each segment, and stores the resulting spectra in a list. For each genre, the average distance between the spectra of the new song and the average spectra of the genre is calculated. The genre with the smallest distance is returned as the most probable genre for the new song.

## Note
This code is a basic implementation of genre recognition using FFT. There are many ways to improve the accuracy of the algorithm, such as using more advanced signal processing techniques or using a larger dataset.
