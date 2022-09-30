inputs: Series(numericSeries), Len(numericsimple);                                                 

variables: nbarAverage(0),nbarDev(0);
	
nbarAverage = Average(Series,Len);
nBarDev = MeanDeviation(Series,len);

if nBarDev = 0 then
	P1014.CCI.MD = 0
else
	P1014.CCI.MD = (Series - nbarAverage)/(0.015*nBarDev);
