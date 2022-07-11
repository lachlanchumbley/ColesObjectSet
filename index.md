# Coles Object Set
## Welcome to the Coles Supermarket Object Dataset

<div style="min-width: 400px; text-align: center; margin-left: auto; margin-right: auto;">
  <img src="{{ site.baseurl }}/images/photos/All Objects.jpeg" alt="image" width="80%"/>
</div>

The dataset consists of 3D water-tight mesh models of 50 supermarket objects.

You can download the dataset [**HERE**](https://bridges.monash.edu/articles/dataset/Supermarket_Object_Dataset/20179550).

The object and model set was created to facilitate benchmarking of computer vision and robotics applications. You can find the Robotic Grasping Dataset that uses a subset of this object set [**HERE**](https://lachlanchumbley.github.io/RealGraspingDataset/).

## The Objects

The objects were picked from 10 different categories:
- Small Box (Food)
- Large Box (Food)
- Regular Cylinder (Food)
- Irregular Cylinder (Food)
- Small Box
- Large Box
- Regular Cylinder
- Irregular Cylinder
- Packet
- Irregular Shapes

<div float="left" style="display: flex; flex-direction: row; flex-wrap: wrap;">
  {% for image in site.static_files %}
      {% if image.path contains 'categories' %}
        {% if image.path contains '.JPG' %}
            {% assign pathsplit = image.path | split: "/" %}
            {% assign length = pathParts.size | minus: 1 %}
            {% assign filesplit = pathsplit[length] | split: "." %}
            <!-- ten percent for ten per row?? -->
            <div style="width: 10%; min-width: 150px; text-align: center; font-size: 60%; margin-left: auto; margin-right: auto;">
              <!-- <strong>Object Name:</strong> {{ filesplit[0] }}  -->
              <div> {{ filesplit[0] }} </div>
              <img src="{{ site.baseurl }}{{ image.path }}" alt="image" width="80%"/>
            </div>
        {% endif %}
      {% endif %}
  {% endfor %}
</div>

## The Models
The models are 3D watertight meshes and are stored as .ply files.
<div float="left" style="display: flex; flex-direction: row; flex-wrap: wrap;">
  {% for image in site.static_files %}
      {% if image.path contains 'gifs' %}
        {% if image.path contains '.gif' %}
            {% assign pathsplit = image.path | split: "/" %}
            {% assign length = pathParts.size | minus: 1 %}
            {% assign filesplit = pathsplit[length] | split: "." %}
            <!-- ten percent for ten per row?? -->
            <div style="width: 30%; min-width: 200px; text-align: center; margin-left: auto; margin-right: auto;">
              <img src="{{ site.baseurl }}{{ image.path }}" alt="image" width="80%"/>
            </div>
        {% endif %}
      {% endif %}
  {% endfor %}
</div>

Here are all the objects in the dataset:

<div float="left" style="display: flex; flex-direction: row; flex-wrap: wrap;">
  {% for image in site.static_files %}
      {% if image.path contains 'models' %}
        {% if image.path contains '.png' %}
            {% assign pathsplit = image.path | split: "/" %}
            {% assign length = pathParts.size | minus: 1 %}
            {% assign filesplit = pathsplit[length] | split: "." %}
            <!-- ten percent for ten per row?? -->
            <div style="width: 20%; min-width: 250px; text-align: center; font-size: 90%; margin-left: auto; margin-right: auto;">
              <!-- <strong>Object Name:</strong> {{ filesplit[0] }}  -->
              <div> {{ filesplit[0] }} </div>
              <img src="{{ site.baseurl }}{{ image.path }}" alt="image" width="80%"/>
            </div>
        {% endif %}
      {% endif %}
  {% endfor %}
</div>

This dataset was developed by Monash University in conjunction with Coles Supermarkets.

<div float="left" style="display: flex; flex-direction: row; flex-wrap: wrap;">
  <div style="width: 45%; min-width: 400px; margin-left: auto; margin-right: auto;">
    <img src="{{ site.baseurl }}/images/logos/Monash_University_logo.png" alt="image" width="80%"/>
  </div>
  <div style="width: 45%; min-width: 400px; margin-left: auto; margin-right: auto;">
    <img src="{{ site.baseurl }}/images/logos/Coles_logo.png" alt="image" width="80%"/>
  </div>
</div>
