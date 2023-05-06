# Vaulting

See https://www.youtube.com/watch?v=HVhH2qi2B5Q Gorka Games RPG tutorial Episode 3.

If you have trouble getting your vault working, here is the first step that can be tested to see if your vault is correct so far.

Check list:
* Did you turn on the Motion Warping plugin?
* Did you restart the editor?

<img src="images\vault-stage-01.png">

In the next image, you can see all three sphere traces, and two have hits.

<img src="images\vault-01-trace-example-two-hits.png">

Below, you can see 2 sphere traces coming from the player. Trace 0 misses the red barrier block. Trace 1 hits the block, and so far our blueprint is set to stop after we get a hit. This happens after Stage 1 of the blueprint is completed, and you connect the **True** pin from the first branch node back to the **Break** pin of the first **For Loop With Break** node.

<img src="images\vault-01-trace-example.png">

## Stage 02 - Forward Distance

The Stage 2 Blueprint shows the **Branch** and **Break Hit Result** nodes coming directly from the **Sphere Trace by Channel** node in the Stage 1 blueprint.

Click the image to enlarge it if necessary. 

The value `100` subracted to find the end trace location can also be converted to a parameter to make it easier to fine tune your vaulting.

<img src="images\vault-02-calc-forward-distance-blueprint.png">
