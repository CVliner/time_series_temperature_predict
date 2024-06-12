### Using real world data

In this project you should predict daily temperature based on given csvfile.
Begin by looking at the structure of the csv that contains the data:
As you can see, each data point is composed of the date and the recorded minimum temperature for that date.
In the first exercise you will code a function to read the data from the csv but for now run the next cell to load a helper function to plot the time series.

Now you need to read the data from the csv file. To do so, complete the `parse_data_from_file` function.

A couple of things to note:

- You should omit the first line as the file contains headers.
- There is no need to save the data points as numpy arrays, regular lists is fine.
- To read from csv files use `csv.reader` by passing the appropriate arguments.
- `csv.reader` returns an iterable that returns each row in every iteration. So the temperature can be accessed via row[1] and the date can be discarded.
- The `times` list should contain every timestep (starting at zero), which is just a sequence of ordered numbers with the same length as the `temperatures` list.
- The values of the `temperatures` should be of `float` type. You can use Python's built-in `float` function to ensure this.

 Forecast should achieve a MSE of 6 or less and a MAE of 2 or less

- If your forecast didn't achieve this threshold try re-training your model with a different architecture (you will need to re-run both `create_uncompiled_model` and `create_model` functions) or tweaking the optimizer's parameters.
