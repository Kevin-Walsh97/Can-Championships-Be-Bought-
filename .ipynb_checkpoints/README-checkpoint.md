# Can-Championships-Be-Bought-

*** Research Questions:
    1) Do taller NBA teams have more success?
    2) Do NBA teams who have a higher aggregate team salary have more success?
        Success measured by:
        Comparing the average total points a team scores ("Points_Scored") vs. average total points a team allows ("Points_Allowed") over a subset of NBA seasons
        Monte carlo simulation will be run to compare two teams (tallest vs. shortest and highest paid vs. lowest paid) producing a winning percentage based on Points_Scored vs. Points_Against simulating x number of games

        Question for Group: Should we compare to a baseline of success such as overall team win/loss record?

    3) Can we identify any key correlations between number of wins in a season and key offensive stats other then points such as;
            Offensive Rebounds
            Assists
            Field Goal Attempts
            Field GOals Made
            Field Goal Percentage
            3 Pointer Attempts
            3 Pointers Made
            3 Pointers Percentage 

    4) Does the region / market a team play in have any correlation to salary spent and/or number of wins across the data set


*** Datasets being used
    All 30 NBA Teams
        Location of each team: Longitute, Latitude
    Yearly data from 2008 to 2017 seasons for each team:
        Team Name
        Wins
        Losses
        Average Points Scored per season
        Average Points Allowed per season
        Average player higher per team per season
        Aggregate team salary per team per season
        Key offensive stats for correlation analysis
            Offensive Rebounds
            Assists
            Field Goal Attempts
            Field GOals Made
            Field Goal Percentage
            3 Pointer Attempts
            3 Pointers Made
            3 Pointers Percentage 


*** Process:
    Aggregate and clean data into one dataframe for analysis (Jupyter Notebook 1)

    Perform analysis to select teams for monte carlo simulation
        Selecting teams
            For each year compare and rank teams by
                Aggregate height and aggregate salary   
                    Decision Point: Do we want to create an index for every team in the data set (DET_2009_Salary_23) would mean that across all years, the Detriot 2009 team had the 23rd highest salary???  Doing this would create two lists; one for salary and then another for height and would allow us to run the monte carlo choosing teams from different years based on the parameters selected (tallest team in 2008 vs. shortest team in 2014)

        Need to show normal distribution
            For each unique team_year can we create a drop down that wil chart out in a histogram Points_Scored and Points_Allowed ?  This could be an interactive plot/view
        
        Components for the monte carlo needed for each team:
            For each unique team_year need
                Points_Scored.mean()  ---> DET_2009_Points_Scored.mean()
                Points_Scored.std()  ---> DET_2009_Points_Scored.std()

                Points_Against.mean()  ---> DET_2009_Points_Against.mean()
                Points_Against.std()  ---> DET_2009_Points_Against.std()

        Run the monte carlo
            Need to select two teams to compare: Focus on height and salary for presentation but build model for any teams to be compared??
            Use gauss function to randomly select mean and std
                random.gauss(100,15)

                 Need to work out coding calculation as we arent using an API but our csv data files...

*** Illustrations:
    1. Drop down visualization by year:  Team Salary vs. Wins
    2. Drop down visualization by year: Team Height vs. Wins
    3. Map Plot - plot team locations with heighhts and salaries
    4. Histogram showing normal distribution of Points_Scored 
    5. Histogram showing normal distribution of Points_Allowed
    6. Conclusion graphic that answers research questions; 
        a) do teams win more with a higher payroll 
        b) do teams win more with more height
        c) are there other offensive correlations we have identified [how does this fit in?]


