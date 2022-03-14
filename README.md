# Beautifly_B
Beautifly_B is an open-source Python library that generates beautiful, high-density visualizations to kickstart EDA (Exploratory Data Analysis) with just Few lines of code. Output is a fully self-contained HTML application.

The system is built around quickly visualizing target values and comparing datasets. Its goal is to help quick analysis of target characteristics other such data characterization tasks.

Example code
from demo import say_hello
say_hello()
...
"# Beautifly_B" 
_____________
Features
-----------------------------------------------------------------------------------------------------------------
- **Target analysis** 
  - Shows how a target value (e.g. "Survived" in the Titanic dataset) relates to other features
- **Visualize and compare**
  - Distinct datasets (e.g. training vs test data)
  - Intra-set characteristics (e.g. male versus female)
- **Mixed-type associations**
  - Sweetviz integrates associations for numerical (Pearson's correlation), categorical (uncertainty coefficient) and categorical-numerical (correlation ratio) datatypes seamlessly, to provide maximum information for all data types.
- **Type inference**
  - Automatically detects numerical, categorical and text features, with optional manual overrides 
- **Summary information** 
  - Type, unique values, missing values, duplicate rows, most frequent values
  - Numerical analysis: 
    - min/max/range, quartiles, mean, mode, standard deviation, sum, median absolute deviation, coefficient of variation, kurtosis, skewness
-----------------------------------------------------------------------------------------------------------------
Upgrading 
-----------------------------------------------------------
Some people have experienced mixed results behavior upgrading through pip. To update to the latest from an existing install, it is recommended to pip uninstall Beautifly_B first, then simply install.

-----------------------------------------------------------------------------------------------------------------
Using pip
-----------------------------------------------------------------------------------------------------------------
The best way to install sweetviz (other than from source) is to use pip:

pip install Beautifly_B

Basic Usage
-----------------------------------------------------------------------------------------------------------------
### cleaning_missing()
```
cleaning_missing(  self, input_vars=[])
```            
**cleaning_missing(...)** scan each column, indicating if droping or keeping the variable for 
            modelling and why, for the ones keeping indicates which cleaning / transformation 
            is recommended for the missing values and if scalling / dummy creation is recommended, 
            if not always inform that is not necessary
- **layout**: Either `'widescreen'` or `'vertical'`. The widescreen layout displays details on the right side of the screen, as the mouse goes over each feature. The new (as of 2.0) vertical layout is more compact horizontally and enables expanding each detail area upon clicking.
- **scale**: Use a floating-point number (`scale= 0.8` or `None`) to scale the entire report. This is very useful to fit reports to any output.
- **open_browser**: Enables the automatic opening of a web browser to show the report. Since under some circumstances this is not desired (or causes issues with some IDE's), you can disable it here.

### show_notebook()
```
show_notebook(  w=None, 
                h=None, 
                scale=None,
                layout='widescreen',
                filepath=None)
```            
**show_notebook(...)** is new as of 2.0 and will embed an IFRAME element showing the report right inside a notebook (e.g. Jupyter, Google Colab, etc.). 

Note that since notebooks are generally a more constrained visual environment, it is probably a good idea to use custom width/height/scale values (`w`, `h`, `scale`) and even **set custom default values in an INI override** (see below). The options are:
- **w** (width): Sets the width of the output _window_ for the report (the full report may not fit; use `layout` and/or `scale` for the report itself). Can be as a percentage string (`w="100%"`) or number of pixels (`w=900`).
- **h** (height): Sets the height of the output _window_ for the report. Can be as a number of pixels (`h=700`) or "Full" to stretch the window to be as tall as all the features (`h="Full"`).
- **scale**: Same as for show_html, above.
- **layout**: Same as for show_html, above.
- **scale**: Same as for show_html, above.
- **filepath**: An optional output HTML report.

Delete features that suspected record ID .
-----------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------
Replace categorical features with dummy features 
Split train with  and test 
---------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------
Transformed from object to Weight of Evidence WOE
-----------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------

Apply standard scaling for all input featuresit will provide a HTML page with the following: 
\\Features with Null Values
\\Features Basic Stats
\\Features data types
 \\In addition to different plots

