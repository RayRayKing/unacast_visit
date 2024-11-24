# **Assignment**

**Goal:** Analyze venue visitation patterns and design a scalable processing pipeline   
**Duration:** 45 minutes  - 1 hour

## The Challenge
You have data capturing anonymous individuals visiting specific venues. The data is provided in daily batches (CSV) available in the `./daily_data/` folder with the following structure:

***Data Structure***
The files correspond to visitation data for individual days, stored as follows:

```python
daily_data/
├── 20241028.csv
├── 20241029.csv
├── 20241030.csv
...
```


***Data Schema***
```python
{
    'venue_id': string,             # Venue identifier
    'visitor_id': string,           # Anonymous visitor identifier
    'visit_start_time': datetime,   # Visit start date and time
    'visit_end_time': datetime,     # Visit end date and time
    'venue_type': string            # Type of venue
}
```

### Tasks
1. **Quick Data Analysis**
    * Load and inspect the provided dataset.
    * Familiarize yourself with the data structure.
    * Identify potential data quality issues.


2. **Simple Processing Pipeline**
   * Build a basic pipeline to process the data on a daily basis:
	 - Load the corresponding batch for each day.
     - Handle data inconsistencies.
	 - For each venue and day, perform the following:
	     - Compute the daily visitor count (unique visitors and total).
	     - Predict the next day's visitor count (based on historical values).
     - Append the processed data to a CSV file named `daily_visitation_summary.csv` in the structure described below:
     - 
	```python
	{
	    'date': date,                                  # Processing date
	    'venue_id': string,                            # Venue identifier
	    'visitor_count_unique': integer,               # Number of visits by unique visitors
	    'visitor_count_total': integer,                # Total number of visits (including repeated visits)
	    'visitor_count_total_prediction': float,       # Prediction for total visit count for the next day
	}
	```
   * Focus on pipeline structure and handling rather than prediction accuracy.


### Questions
Answer briefly:
1. How would you scale this pipeline to handle:
   - 20 million locations of 20 million users
   - Real-time updates
2. How would you store the data?
3. How would you monitor data quality?
4. What would your daily orchestration look like?


## Deliverables
1. **Python Notebook or Script**
   - Data processing code.
   - Basic prediction pipeline.
   - Clear comments.
   - Instructions how to run the code.

2. **Report with a Brief Summary**
   - Key findings.
   - Answers to the questions above.
   - Any assumptions made.

## Evaluation Focus
- Code structure and clarity
- Data pipeline design
- Error handling
- Scaling considerations

## Notes
- For simplicity, the example includes dummy data of a small magnitude. Consider how your solution would work in a real production environment at scale.
- Focus on writing production-ready code over complex algorithms.
- You can use any standard Python data libraries

**How to submit:**
- Upload to a Github repository and share the project with jan.benetka@unacast.com.

**Next steps:**
- 15-20 min discussion of your solution with a person(s) from Unacast.


---

We know assignments like this take time, and we really appreciate the effort you're putting into it. It’s all about making sure our team is packed with the best and brightest, and honestly, we’re rooting for you to be one of us. We really hope this isn’t the last time we get to write some code together!

---

 🚀 Thanks for your time and effort – we hope you’ll join us! 🚀
