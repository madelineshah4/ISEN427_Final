# ISEN427_Final

In this project, we build a Bayesian logistic model to analyze the precision of calls made by MLB umpires. We work with datasets containing pitch information and umpire decisions for 3 individual umpires.

We build several Bayesian logistic models of precision for each umpire, each containing different subsets of important features. Then, we compare the models using the posterior predictive and determine the most relevant features in an umpire's decision.

## Column Descriptions
- The x axis represents horizontal position, y represents distance from pitcher to catcher, and z represents the height of the ball.

### Count Information
- **balls**: Pre-pitch number of balls in count.  
- **strikes**: Pre-pitch number of strikes in count.  

### Pitch Type
- **pitch_type**: The type of pitch derived from Statcast.  
&nbsp; - **pitch_type_CH to pitch_type_SV** *(encoded)*: One-hot encoded boolean indicators for pitch types such as CH (Changeup), SL (Slider), etc.  

### Pitch Characteristics
- **release_speed**: Pitch velocity, measured out-of-hand for recent data.  
- **release_pos_x**: Horizontal release position (feet) from the catcher's perspective.  
- **release_pos_y**: Release position (depth) from the catcher's perspective.  
- **release_pos_z**: Vertical release position (feet) from the catcher's perspective.  
- **vx0**: Velocity of the pitch in the x-dimension (feet/sec), determined at y=50 feet.  
- **vy0**: Velocity of the pitch in the y-dimension (feet/sec), determined at y=50 feet.  
- **vz0**: Velocity of the pitch in the z-dimension (feet/sec), determined at y=50 feet.  
- **ax**: Acceleration of the pitch in the x-dimension (feet/sec²), determined at y=50 feet.  
- **ay**: Acceleration of the pitch in the y-dimension (feet/sec²), determined at y=50 feet.  
- **az**: Acceleration of the pitch in the z-dimension (feet/sec²), determined at y=50 feet.  

### Ball Movement and Location
- **pfx_x**: Horizontal movement in feet from the catcher's perspective.  
- **pfx_z**: Vertical movement in feet from the catcher's perspective.  
- **plate_x**: Horizontal position of the ball when it crosses home plate.  
- **plate_z**: Vertical position of the ball when it crosses home plate.  
- **pitch_location**: Distance of the pitch from the boundary of the strike-zone.  
- **zone**: Zone location of the ball when it crosses the plate.  

### Batter and Pitcher Context
- **stand**: Side of the plate the batter is standing.  
&nbsp; - **stand_R** *(encoded)*: True if batter is standing on the right side.  
- **p_throws**: Hand the pitcher throws with.  
&nbsp; - **p_throws_R** *(encoded)*: True if pitcher throws right-handed.  
- **all_star_player**: Indicates if the pitcher has played in an All-Star game.  

### Game Context
- **game_year**: Year the game took place.  
- **home_score**: Pre-pitch home team score.  
- **away_score**: Pre-pitch away team score.  
- **delta_home_win_exp**: Change in win expectancy before and after the plate appearance.  
- **delta_run_exp**: Change in run expectancy before and after the pitch.  
- **pitch_number**: Total pitch number in the plate appearance.   

### Strike Zone
- **sz_top**: Top of the batter's strike zone set by the operator.  
- **sz_bot**: Bottom of the batter's strike zone set by the operator.  

### Target
- **description**: Description of the resulting pitch.  
&nbsp; - **description_called_strike** *(encoded)*: Indicates if the pitch was called a strike `0` or ball `1`.
&nbsp; - **error_in_decision** *(encoded)*: Binary target variable. `1` indicates the umpire made an incorrect call, `0` indicates a correct call.  
