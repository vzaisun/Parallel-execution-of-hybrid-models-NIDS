The code creates a model_function list which has three sepereate model generation functions: create_model_1, create_model_2, and create_model_3
By utilizing the Pool class, the script achieves parallelization of model training and prediction tasks.
The starmap function is employed to map the train_model function to each model in model_functions, passing the necessary arguments including the model function, input shape, number of classes, training and validation data.
Weights are allocated to each model in the weight list, signifying their relative contribution to the ensemble setup.
Predictions are calculated by aggregating the weighted prediction of each model using the weighs that have been assigned.
The script determines the final ensemble prediction by selecting the class with the highest sum of weighted average.
