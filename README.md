Given a Fahrenheit temperature it is possible to calculate the corresponding Celsius temrerature with the help of the following formula:
c = 5 / 9 * (f - 32) 


In this formula  f is the  independent variable and variable c is the  dependent variable because each value of c depends on the value of f .


The result of plotting Fahrenheit temperatures and their corresponding Celsius is a straight line. 

c = lambda f: 5 / 9 * (f - 32) :first we create a lambda for our formula to calculate the Celsius equivalent of the Fahrenheit temperatures for O to 100 in 10 degree incements. 
temps = [(f, c(f)) for f in range(0, 101, 10)]  :we store each Fahrenheit/Celsius pair as a tuple in pairs 
temps_df = pd.DataFrame(temps, columns=['Fahrenheit', 'Celsius']) :next ,we place our data in a Data Frame 
axes = temps_df.plot(x='Fahrenheit', y='Celsius', style='.-') :we use the plot method in order to display the linear relationship between the Fahrenheit and Celsius temperatures 
