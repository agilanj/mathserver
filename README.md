# Ex.05 Design a Website for Server Side Processing
# Date: 02-12-2024
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
~~~



<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Power of a lamp</title>
    <style>
        body {
            background-color: black;
            font-family: 'Lora', serif;
        }
        .container {
            width: 600px;
            margin: 100px auto;
            text-align: center;
            background-color: whitesmoke;
            color: black;
            padding: 20px;
            border: 3px  rgb(3, 16, 19);
            border-radius: 5px;
        }
        input[type="text"] {
            width: 90%;
            padding: 5px;
            margin: 20px 0;
        }
        input[type="submit"] {
            padding: 5px 10px;
            background-color: rgb(193, 2, 72);
            color: rgb(3, 246, 145);
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
    <h1>Power of a lamp</h1>

    <form method="POST">
        {% csrf_token %}
        <label for="intensity">Intensity (I in Amps):</label>
        <input type="text" name="intensity" id="intensity" required><br><br>

        <label for="resistance">Resistance (R in Ohms):</label>
        <input type="text" name="resistance" id="resistance" required><br><br>
        <font ="red">
        <button type="submit"><b>calculate</b></button>
    </font>
    </form>

    {% if power is not None %}
        <h2>Calculated Power: {{ power }} Watts</h2>
    {% endif %}
</div>
</body>
</html>


~~~
# SERVER SIDE PROCESSING:

![Screenshot (90)](https://github.com/user-attachments/assets/050e84d8-2e51-45ba-ac60-12e838fa433d)

# HOMEPAGE:
![Screenshot (91)](https://github.com/user-attachments/assets/362a1f17-cda2-48aa-88ed-f8e5efa9f38d)


# RESULT:
The program for performing server side processing is completed successfully.
