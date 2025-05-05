# DAX Examples and Use Cases

Emails that were sent to my Major to assist him with building a DAX formula the formula allowed us to take Document Number of parts 
such as WNX434WNX and extract the 434, this was necessary to allow a count of only specific items.

Email sent teaching DAX to MAJ: 

1st you must create a new column, to do so be in report view, go to modeling at the top > new column > Enter DAX function


```DAX
Extract 3 digits = MID('Sheet1'[DoD Document Number], 4, 3)
```

#Calculate Rows 

Email with DAX resolution to a problem:

Go to Model view and click New Measure in the Ribbon

```DAX
Count 2 = CALCULATE( COUNTROWS('ZPOD Report') , FILTER('ZPOD Report', LEFT('ZPOD Report'[Supply Category Material Code], 1) = "2"))
```

```DAX
Count 9 = CALCULATE( COUNTROWS('ZPOD Report') , FILTER('ZPOD Report', LEFT('ZPOD Report'[Supply Category Material Code], 1) = "9"))
```

# Email Sent Debugging Errors:

In the reports I think I have fixed the errors for the Z reports at least the data now loads on my end.

Then do the same to the Conditional Column (custom column). Then Refresh.
