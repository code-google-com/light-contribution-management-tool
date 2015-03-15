# Introduction #

If you need to know how to use LCMT using the Current UI this is the place for you!
This UI explanation is valid for current versions LCMT v 3.1.1 (stable version), LCMT v3.2 (Basic Vray Support)

# UI explanation #

The UI looks like this:

![http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_ui.png](http://www.sfdm.scad.edu/faculty/mkesson/vsfx705/wip/best/spring12/nestor_prado/images/projects/p4_lcmt_ui.png)

**1: Light Type Manager**
  * This dropdown menu allows the artist to Add new light types, view which ones are used in the group lights functionality and reset the types to a default set of types.
**2: Lights in the Scene**
  * Here is where all the "available" lights in the scene can be managed. Clicking on a light name or group name (if use Groups is enabled) selects that light/s. The artist can then acces their attributes in the attribute editor and render the contribution of the lights and view the result in the renderview.
**3: Group Lights**
  * When this checkbox is enabled the light list is automatically updated with the different light groups found on the scene. The light groups are made based on the light types explained in paragraph 1.
**4: Save images? (Yes Please)**
  * When this functionality is enabled the renders created when hitting the render lights button will be automatically saved in the project's images/tmp/ folder for easy access. These images are saved as sceneName\_contributionOf\_nameofLight1_..._nameofLightN.iff. Once saved they will be updated each time the corresponding lights are rendered using LCMT. That allows the artist to load these images in a compositing software such as Nuke and start pre-comping the image and only having to reload the image corresponding to the changes made in maya. In the current version of LCMT the images are only saved as .iffs. Further versions of LCMT should be able to writeout any type of image file that Maya supports.
**5: Render Lights**
  * Here is where the magic happens! Hitting this button will automatically render the contribution of any light selected. The lights can be selected in the LCMT interface or in the outliner. If no lights are currently selected when the button is pressed each individual light will be rendered seperately.
**6: Geometry list**
  * This list shows all the geometry in the scene. As with the light list selecting an element or elements of this list will select the correspondant geometry in the scene. This list is mainly used to select specific geometry that the artist wants to include in the render layers that can be automatically created by pressing the Create Render Layers! button below.
**7: Create Render Layers!**
  * By pressing this button LCMT will automatically create some render layers depending on the selections.
    1. If some lights are selected and some geometry is selected a single render layer will be created including said selection.
    1. If some geometry is selected a series of render layers will be created including the geometry selected and one layer per light group.
  * This functionality allows the artist to take all the tediousness out of creating render layers with different lights.