# lab02-debugging

https://www.shadertoy.com/view/tfsBDf

Syntax error: vec doesn't exist, should be vec2

Camera error: The line H *= len * iResolution.x / iResolution.x incorrectly calculates horizontal camera vector, causing image to stretch along x

Raycast bug: UV used to create camera rays is uv (0 to 1) instead of uv2 (-1 to 1), UV should be from -1 to 1, 0 to 1 only calculates rays in one camera quadrant

Raymarch for loop: requires more iterations to hit the floor behind the spheres, since raymarch steps are smaller when the ray is closer to sphere

Reflect error: dir = reflect(eye, nor) wrongly reflects the eye position instead of the ray direction when calculating reflection


# Setup 

Create a [Shadertoy account](https://www.shadertoy.com/). Either fork this shadertoy, or create a new shadertoy and copy the code from the [Debugging Puzzle](https://www.shadertoy.com/view/flGfRc).

Let's practice debugging! We have a broken shader. It should produce output that looks like this:
[Unbelievably beautiful shader](https://user-images.githubusercontent.com/1758825/200729570-8e10a37a-345d-4aff-8eff-6baf54a32a40.webm)

It don't do that. Correct THREE of the FIVE bugs that are messing up the output. You are STRONGLY ENCOURAGED to work with a partner and pair program to force you to talk about your debugging thought process out loud.

Extra credit if you can find all FIVE bugs.

# Submission
- Create a pull request to this repository
- In the README, include the names of both your team members
- In the README, create a link to your shader toy solution with the bugs corrected
- In the README, describe each bug you found and include a sentence about HOW you found it.
- Make sure all three of your shadertoys are set to UNLISTED or PUBLIC (so we can see them!)
