# R-18-Feb-2020 - ML Results from 18 Feb 2020

Results and models for the paper `A Machine Learning Platform for the Discovery of Materials` (Belle, Aksakalli, Russo).

## Notes

There are two approaches to use these models.

### Online

These models are made available for use via a web interface at https://hadokenmaterials.io/ - pop in the relevant figures and off you go. Easy! Also available is an API which you can call to make predictions. These interactions can be as simple as:

**POST**

```
{
	"stoichiometry": "Ca2Cu2Ge4O12"
}
```

**RESPONSE**

```
{
	"bandGap": 1.3985653904114555472784324321,
	"stoichiometry": "Ca2Cu2Ge4O12"
}
```

**NOTE:** Any use of https://hadokenmaterials.io/ (web interface or API) is bound by the following citing policy: https://hadokenmaterials.io/Home/Citing - please make a note of this.

### Offline

 - Install Keras and appropriate other Python bits
 - Load the model into Keras using the appropriate `H5` and `JSON` files
 - Call the model specifying values for the relevant inputs (note that inputs required for each model differ)
 - Save and load Keras models - https://www.tensorflow.org/guide/keras/save_and_serialize
 - python - How to predict from saved model in Keras ? - https://stackoverflow.com/questions/50227925/how-to-predict-from-saved-model-in-keras

## Directory Structure

* **Data**
	- `2020-Feb-16_23-33-16-PAW_PBE_Reduced_HighSymmetry-v5.00.csv` - dataset used to generate the models
* **Models**
	- **BandGap_NULL_P**
		- `BandGap_NULL_P_Results.csv` - results of the training process, including original <i>E<sub>g</sub></i> values and fit
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.h5` - Keras model output
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.json` - Keras model output
		- `History.png` - loss vs. epoch plot
		- `Output.log` - logging information for the entire process
	- **BandGap_SpaceGroup-Geometry_P**
		- `BandGap_SpaceGroup-Geometry_P_Results.csv` - results of the training process
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.h5` - Keras model output
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.json` - Keras model output
		- `History.png` - loss vs. epoch plot
		- `Output.log` - logging information for the entire process
	- **BandGap_SpaceGroup-HighSymmetry-Derived_P**
		- `BandGap_SpaceGroup-HighSymmetry-Derived_P_Results.csv` - results of the training process
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.h5` - Keras model output
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.json` - Keras model output
		- `History.png` - loss vs. epoch plot
		- `Output.log` - logging information for the entire process
	- **FermiEnergy_Geometry_P**
		- `FermiEnergy_Geometry_P_Results.csv` - results of the training process
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.h5` - Keras model output
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.json` - Keras model output
		- `History.png` - loss vs. epoch plot
		- `Output.log` - logging information for the entire process
	- **GapType-Classifier_P**
		- `GapType-Classifier_P_Results.csv` - results of the training process
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.h5` - Keras model output
		- `EnvP.L100.L50.RELU.RELU.D0.01.E1000.B200.Model.json` - Keras model output
		- `History.png` - loss vs. epoch plot
		- `Output.log` - logging information for the entire process

## Correspondence

All contacts are contained within the paper  - please feel free to contact us as you desire.
