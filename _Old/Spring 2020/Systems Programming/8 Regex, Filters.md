# Regex, Filters
## Filter
* Any program that transforms text

## Pipeline
* **Advantages**
	* Easier debugging
	* Mix and match components
	* Parallel computing
* **Disadvantages**
	* Single threaded

## Useful Filters
### Translate `tr`
* `tr <source set> <target set>`
	* replace source set with target set
* `tr -d <thing to delete>`
	* delete thing

### Extract `cut`
* `cut -d <delimiter> -f <index>`
	* Divide string into array based on delimiter and take the work in the index

