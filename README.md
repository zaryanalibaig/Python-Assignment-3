Assignment 3: Programming for AI
How to run
Unzip data.zip so the data/ folder sits next to Assignment3_Programming_for_AI.ipynb.
Install the libraries: pip install numpy pandas matplotlib pillow.
Open the notebook in Jupyter and choose Kernel > Restart & Run All.

Running it creates dashboard.png, dashboard.pdf and wave.gif in the same folder.

One hard thing

Cleaning the mixed date formats in the weather data. Some dates were YYYY-MM-DD and others DD/MM/YYYY, so letting pandas guess would have gone wrong: 57 of the 60 slash dates are misread as MM/DD, silently swapping day and month for 23 of them and failing on the other 34. I parsed each format separately with an explicit format string and checked the result against the wrong reading.