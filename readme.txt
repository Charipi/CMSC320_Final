Dataframe Explanations:
'hitting' contains data for hitters, with no N/A values
    'pa' = number of plate appearances this hitter had over the season
    'k_percent' = percentage of plate appearances that resulted in a strikeout
    'bb_percent' = percentage of plate appearances that resulted in a walk
    'batting_avg' = percentage of at-bats (plate appearances without walks) that resulted in a hit
    'slg_percent' = batting_avg weighted by the number of bases reached on a hit
    'on_base_percent' = percentage of plate appearances that resulted in reaching a base (mostly hits and walks)
    'on_base_plus_slg' = on_base_percent + slg_percent; regarded as a well-rounded measure of hitting quality
    'babip' = batting_avg on balls in play; can be controlled by where a player hits a ball, but is very random (high and low values are unsustainable)
    'woba' = variant of on_base_percent that gives different weights for each method of reaching base based by the expected runs scored (advanced alternative to on_base_plus_slg)
    'xwoba' = statistic that predicts woba based on launch angle and exit velocity of hit balls; variant of woba that is not effected by opposing defenses
    'sweet_spot_percent' = percentage of times the ball was hit between 8 and 32 degrees (these angles tend to have better results)
    'barrel_batted_rate' = percentage of times the ball was hit in a way that projected a result of at least 0.500 batting_avg and 1.500 slg_percent (very well hit)
    'hard_hit_percent' = percentage of balls hit 95mph or faster
    'avg_best_speed'
    'avg_hyper_speed'
    'z_swing_percent' = percentage of times the batter swung at pitches in the strike zone (good for batter)
    'oz_swing_percent' = percentage of times the batter swung at pitches outside the strike zone (bad for batter)
    'whiff_percent' = percentage of times the batter swung and missed a pitch
    'swing_percent' = percentage of pitches the batter swung at; measures overall aggresiveness
    'pull_percent' = percentage of hit balls that went toward the batter's side
    'straightaway_percent' = percentage of hit balls that went toward the middle of the field
    'opposite_percent' = percentage of hit balls that went to the opposite side of the batter

'pitching' contains data for pitchers, with some N/A values for pitches they don't throw
    'p_era' = earned run average; how many runs does the pitcher give up per 9 innings (per complete game)

The dataframes for specific types of pitches only contain columns relevant to that pitch, with no N/A values (only pitchers that throw this pitch)
    'n_(type)_formatted' = Percentage of pitches thrown by this pitcher that were of this type
    '(type)_avg_speed' = Average speed of pitches of this type
    '(type)_avg_spin' = Average spin rate of pitches of this type; usually allows the pitch to curve more through the air and make it harder to track by the batter
    '(type)_avg_break_x' = Average distance the pitch curves horizontally; again, more movement makes the pitch harder to track
    '(type)_avg_break_z' = Average distance the pitch curves vertically

    Types of pitches: fastballs are the fastest pitches and genearlly improve with more speed. These are the fourseam, sinker, and cutter. The sinker and cutter do benefit from more break. The changeup is meant to complement a fastball by being thrown in a similar manner while being roughly 10mph slower and breaking downwards. The slider and curveball are both slow pitches that benefit from large amounts of break.