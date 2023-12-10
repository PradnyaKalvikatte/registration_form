# registration_form
registratin form coding
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration and login flip-style</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #fad0c4;
        }
        body .form-group input {
        width: 338px; /* or another specific value */
        }


        .form-container {
            transition: transform 0.3s ease-in-out, 0.3s;
            overflow-y: auto;
            justify-content: center;
            max-height: 650px;
            max-width: 450px;  
            background: rgba(255, 255, 255, 0.6);
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.9);
            padding: 20px;
            border-radius: 8px;
            border: 3px solid #9F2365;
        }
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr; /* Two columns in the grid */
            gap: 20px; /* Gap between columns */
        }
        .grid-container1 {
            display: grid;
            grid-template-columns: 1fr 1fr; /* Two columns in the grid */
            gap: 20px; /* Gap between columns */
            
        }

        .form-group {
            position: relative;
            margin-bottom: 20px;
            width: 100%;
        }

        .form-group label {
            position: absolute;
            left: 10px;
            top: 50%;
            transform: translateY(-20%);
            color: #9F2365;
            pointer-events: none;
            transition: 0.3s;
        }

        .form-group input {
            background: transparent;
            color: #9F2365;
            padding: 10px;
            box-sizing: border-box;
            border: 1px solid #9F2365;
            border-radius: 5px;
            transition: 0.3s;
            width: 433px !important;
        }

        .form-group input:focus {
            outline: none;
            border-color: #9F2365;
        }

        .form-group input:focus + label,
        .form-group input:not(:placeholder-shown) + label {
            font-family: Times New Roman;
            font-size: 16px;
            top: 5px;
            color: #9F2365;
        }

        .form-container:hover,
        .form-group input:hover,
        .form-group label:hover {
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);

        }

        .submit-btn {
            background-color: #3498db;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 49.2%;
            margin-left:0px;
        }

        .submit-btn:hover {
            background-color: #0056b3;
        }
        .cancel-btn {
            background-color: #e74c3c;
            color: #fff;
            padding: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            width: 49.3%;
            margin-top: 10px;
            align-items: center;
        }

        .cancel-btn:hover {
            background-color: #c0392b;
        }

        .form-container:hover {
            transform: scale(1.02);
            }

        .h2 {
            color: #9F2365;
            text-align: center;
            font-family: Times New Roman;
            padding-top: 0px;
        }
        .login-form {
            display: none;
            padding: 20px;
        }
       .form-group input:focus + label,
       .form-group input:valid + label {
        transform: translateY(-120%);
        font-size: 12px;
        color: #9F2365;
        }
       .role-dropdown {
        position: relative;
        margin-bottom: 20px;
        }

        .role-dropdown select {
            background: transparent;
            width: 100%;
            padding: 10px;
            box-sizing: border-box;
            border: 1px solid #9F2365;
            border-radius: 5px;
            transition: 0.3s;
        }

        .role-dropdown select:focus {
            outline: none;
            border-color: #9F2365;
        }

        .role-dropdown label {
        position: absolute;
        left: 10px;
        top: 50%;
        transform: translateY(-120%);
        color: #9F2365;
        pointer-events: none;
        transition: 0.3s;
        }

        .role-dropdown select:focus + label,
        .role-dropdown select:not(:placeholder-shown) + label {
            font-family: Times New Roman;
            font-size: 16px;
            top: 5px;
            color: #9F2365;
        }
        .form-group input:hover,
        .form-group label:hover {
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
        }

        .role-dropdown:hover select,
        .role-dropdown select:hover + label,
        .role-dropdown select:not(:placeholder-shown) + label {
        box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.3);
        }
    </style>
</head>
<body>

    <div class="form-container" id="registrationForm" >
        <form>
            <h2 class="h2">Register Here!</h2>
            <br>
             <div class="grid-container">
            <!-- Your registration form content -->
             <div class="role-dropdown form-group">
                <select id="role" name="role" style="color: #9F2365" required>
                    <option value="" disabled selected>Register as</option>
                    <option value="student">Student</option>
                    <option value="teacher">Teacher</option>
                    <option value="principal">Principal</option>
                </select>
            </div>
             <div class="role-dropdown form-group">
                <select id="gender" name="gender" style="color: #9F2365"  required>
                    <option value="" disabled selected >Gender</option>
                    <option value="student">Male</option>
                    <option value="teacher">Female</option>
                    <option value="principal">Others</option>
                </select>
                <label for="gender" style="box-shadow: none;" ></label>
            </div>
        </div>
            <div class="role-dropdown form-group" >
                <input type="file" id="image" name="image" accept="image/*" style="color:#9F2365;">
                <label for="image" style="color:#9F2365;">Image</label>
            </div>
              <div class="role-dropdown form-group">
                <input type="tel" id="phone" name="phone" required >
                <label for="phone">Phone No.</label>
            </div>

            <div class="form-group">
                <input type="text" id="username" name="username" required >
                <label for="username">Username</label>
            </div>
            <div class="form-group">
                <input type="password" id="password" name="password" required>
                <label for="password">Password</label>
            </div>
             <div class="form-group">
                <input type="email" id="email" name="email" required>
                <label for="email">Email</label>
            </div>
           
            <div class="form-group">
                <input type="text" id="address" name="address" required>
                <label for="address">Address</label>
            </div>
            <div class="form-group">
                <input type="text" id="position" name="position" required>
                 <label for="position">Position</label>
            </div>
            <div class="form-group">
                <input type="text" id="department" name="department" required>
                 <label for="department">Department</label>
            </div>
            <div class="form-group">
                 <input type="text" id="qualification" name="qualification" required>
                <label for="qualification">Qualification</label>
            </div>
            <div class="form-group">
                <input type="text" id="experience" name="experience" required>
                <label for="experience">Professional Experience</label>
            </div> 
            <div class="form-group">
                <button type="submit" class="submit-btn">Register</button>
                <button type="button" class="cancel-btn" onclick="cancelRegistration()">Cancel</button>
            </div>
            
            <p onclick="toggleForm()">Already have an account?<span style="color:#9F2365;"> Login</span></p>
            
        </form>
    </div>
    <div class="form-container login-form" id="loginForm" style="width: 450px">
        <form>
            <h2 class="h2">Login Here!</h2>
            <!-- Your login form content -->
            <div class="role-dropdown form-group">
                <select id="role" name="role" style="color: #9F2365" required>
                    <option value="" disabled selected>Register as</option>
                    <option value="student">Student</option>
                    <option value="teacher">Teacher</option>
                    <option value="principal">Principal</option>
                </select>
            </div>
            <div class="grid-container1" >
            <div class="form-group">
                <input type="text" id="loginUsername" name="loginUsername" required style="font-size: 16px;">
                <label for="loginUsername">Username</label>
            </div>
            <div class="form-group">
                <input type="password" id="loginPassword" name="loginPassword" required>
                <label for="loginPassword">Password</label>
            </div>
        </div>
            <div class="form-group">
                <button type="submit" class="submit-btn">Login</button>
                <button type="button" class="cancel-btn" onclick="cancelRegistration()">Cancel</button>
            </div>
            <p onclick="toggleForm()">Don't have an account? <span style="color:#9F2365">Register</span></p>
        </form>
    </div>
</div>
    <script>
        function toggleForm() {
            var registrationForm = document.getElementById('registrationForm');
            var loginForm = document.getElementById('loginForm');
            if (registrationForm.style.display === 'none') {
                registrationForm.style.display = 'flex';
                loginForm.style.display = 'none';
            } else {
                registrationForm.style.display = 'none';
                loginForm.style.display = 'flex';
            }
        }
         function cancelRegistration() {
            document.getElementById('registrationForm').reset();
        }
    </script>
</body>
</html>

