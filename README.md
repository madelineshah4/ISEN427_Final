# ISEN427_Final

In this project, we build a Bayesian logistic model to analyze the precision of calls made by MLB umpires. We work with datasets containing pitch information and umpire decisions for 3 individual umpires.

We build several Bayesian logistic models of precision for each umpire, each containing different subsets of important features. Then, we compare the models using the posterior predictive and determine the most relevant features in an umpire's decision.

Below are descriptions of key columns included in the dataset.

Column Descriptions
balls: Pre-pitch number of balls in count.
strikes: Pre-pitch number of strikes in count.
pitch_type: The type of pitch derived from Statcast.
release_speed: Pitch velocity, measured out-of-hand for recent data.
release_pos_x: Horizontal release position (feet) from the catcher's perspective.
release_pos_z: Vertical release position (feet) from the catcher's perspective.
description: Description of the resulting pitch.
zone: Zone location of the ball when it crosses the plate from the catcher's perspective.
stand: Side of the plate the batter is standing.
p_throws: Hand the pitcher throws with.
game_year: Year the game took place.
pfx_x: Horizontal movement in feet from the catcher's perspective.
pfx_z: Vertical movement in feet from the catcher's perspective.
plate_x: Horizontal position of the ball when it crosses home plate from the catcher's perspective.
plate_z: Vertical position of the ball when it crosses home plate from the catcher's perspective.
on_3b: Pre-pitch MLB Player ID of the runner on 3rd base.
on_2b: Pre-pitch MLB Player ID of the runner on 2nd base.
on_1b: Pre-pitch MLB Player ID of the runner on 1st base.
delta_home_win_exp: Change in win expectancy before and after the plate appearance.
delta_run_exp: Change in run expectancy before and after the pitch.
vx0: Velocity of the pitch in the x-dimension (feet/sec), determined at y=50 feet.
vy0: Velocity of the pitch in the y-dimension (feet/sec), determined at y=50 feet.
vz0: Velocity of the pitch in the z-dimension (feet/sec), determined at y=50 feet.
ax: Acceleration of the pitch in the x-dimension (feet/sec²), determined at y=50 feet.
ay: Acceleration of the pitch in the y-dimension (feet/sec²), determined at y=50 feet.
az: Acceleration of the pitch in the z-dimension (feet/sec²), determined at y=50 feet.
sz_top: Top of the batter's strike zone set by the operator.
sz_bot: Bottom of the batter's strike zone set by the operator.
release_pos_y: Release position of the pitch in feet from the catcher's perspective.
at_bat_number: a counter for how many times a batter has come up to bat during that specific game
pitch_number: Total pitch number in the plate appearance.
home_score: Pre-pitch home team score.
away_score: Pre-pitch away team score.
error_in_decision: Indicates if the decision was correct or incorrect.
pitch_location: Distance of the pitch from the boundary of the strike-zone.
all_star_player: Indicates if the pitcher has played an All star game.
For more information, visit the Statcast CSV Documentation.


"description" and "error_in_decision" are target vars.