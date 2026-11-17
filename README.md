# County Rainfall and Planting Advisory

## Project Summary

This project cleans hand-typed monthly rainfall data from a Machakos weather station, combines it with four clean county datasets (Nairobi, Nakuru, Kisumu, Mombasa) into a 5 x 12 NumPy array, and analyses it to recommend planting windows for a farmer-support NGO. It calculates annual totals, monthly averages, the wettest month per county, dry-month counts (below 50 mm) and the best two-consecutive-month planting window, using vectorised NumPy operations rather than Python loops wherever possible. Results are saved to `rainfall\_summary.csv`.

## How to Run the Notebook

1. Clone the repository: `git clone https://github.com/karondonethan/plp-da-a2-rainfall-advisory.git`
2. Move into the folder: `cd plp-da-a2-rainfall-advisory`
3. Install dependencies: `pip install -r requirements.txt` (and `pip install notebook` if Jupyter is not installed)
4. Launch Jupyter: `jupyter notebook rainfall\_analysis.ipynb`
5. Choose Kernel > Restart \& Run All to reproduce every output and regenerate `rainfall\_summary.csv`.

## Planting Advisory

* Nairobi, Nakuru, Kisumu and Mombasa should plant in April-May, the two consecutive months with the highest combined rainfall in each county.
* Machakos should plant in November-December instead, so its SMS advice must differ from the other four counties, and it is the driest county with six months below 50 mm.
* Machakos data was hand-typed and two months (April and September) were imputed with the rounded mean of 68 mm, so its totals and dry-month count should be verified against station records.

