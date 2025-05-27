# Ex.05 Design a Website for Server Side Processing
## Date: 08-05-2025
# NAME : MOHAMED HAFEEZ S
# REG NO : 212224040193

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :

from flask import Flask, request

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def power():
    if request.method == 'POST':
        V = float(request.form['voltage'])
        I = float(request.form['current'])
        P = V * I
        return f"Power = {P:.2f} Watts"
    return '''
        <form method="post">
            Voltage (V): <input name="voltage" type="number" step="any" required><br>
            Current (A): <input name="current" type="number" step="any" required><br>
            <input type="submit" value="Calculate">
        </form>
    '''

if __name__ == '__main__':
    app.run()

## SERVER SIDE PROCESSING:


## HOMEPAGE:


## RESULT:
The program for performing server side processing is completed successfully.
