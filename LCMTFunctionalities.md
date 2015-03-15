# Introduction #

We will explain the functionalities that LCMT provides Lighting Artists

# Lighting Stage #

LCMT allows the artist to take all the tediousness out of isolating individual lights or light groups to inspect their lighting contribution on the scene.

Let's use some simple examples to illustrate the usefullness of LCMT.

**Dealing with lighting Rigs**
  * When in a production when the artist is given a lighting rig which he knows nothing about the first step he normally has to do is inspect the lights in the light rig one by one to discifer which lights are contributing to which parts of the rendered image. With simple light rigs that could not be seen as a tedious task but with more involved lighting rigs this process can become very long.

**Look developing or lighting a scene from scratch**

  * When lighting a complex scene with a lot of lights contributing differently to different parts of the scene finding out which light is doing what can become a very daunting task.

  * In this example a recreation of a scene from the movie Jarhead, the final light setup used to construct the final lighting involved about 20+ lights.

![http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_example1.png](http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_example1.png)

  * Having had LCMT the task of tweaking individual light colors or different shadows would have been a lot easier and quicker.

# Render Wrangling Stage (Render Layer Creation) #

There are some lighting artists that like to have as much control of their lighting until the latest stages of compositing. One common approach used to have some re-lighting capabilities during the compositing stage is taking advantage of the additive properties of light. This allows the artist to render each light in a seperate layer and combine them in the compositing stage to obtain the original render. There is more information and examples regarding how this method is used in the Alpha Version Write-Up of the LCMT.

If this approach is used it becomes very easy to effectively do some tweaks to individual lights without having to re-render anything, which can be the difference between meeting a deadline or not.

But setting up all the passes to enable this compositing capabilities can become a tedious task that can sometimes can work against using this approach. Luckly this is where LCMT comes into place. With a touch of a button render layers with the selected geometry from the scene are created. Each of them containing a part from the geometry the different light groups in the scene.

Here is an example that shows the LCMT in action

**What we have in a scene**

  * So for example if we have the current scene:

![http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_01.png](http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_01.png)

  * As we can see we have some geometry and some lights. LCMT will create custom Render Layers with the geometry in the scene and each of the light groups found in the scene.

**What LCMT gives us instantly**

  * We execute LCMT and in a fraction of second we have our new render layers ready to render out. In this case we end up with a layer for the:

  1. Background Lights
  1. Bounce Lights
  1. IBL Light (mentalrayIBLNodeShape)
  1. Key Light
  1. Kick Lights

![http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_layers.png](http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_layers.png)