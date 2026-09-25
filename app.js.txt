// --- INITIALISE MOCK STOCK DATA IN LOCALSTORAGE IF EMPTY ---
if (!localStorage.getItem('inventory')) {
    const defaultInventory = [
        { id: "P001", name: "Laptop Batteries", stock: 12, supplier: "Apex Power Ltd", minStock: 15 },
        { id: "P002", name: "Type-C HDMI Hubs", stock: 45, supplier: "LogiTech Logistics", minStock: 10 },
        { id: "P003", name: "Mechanical Keyboards", stock: 4, supplier: "Clicky Switches Corp", minStock: 8 }
    ];
    localStorage.setItem('inventory', JSON.stringify(defaultInventory));
}

// --- MODULE REDIRECTION & ROUTING ---
function handleLogin(event) {
    event.preventDefault();
    const email = document.getElementById('login-email').value;
    const role = document.getElementById('login-role').value; // 'admin' or 'user'

    // Simple session storage to remember who is logged in
    localStorage.setItem('currentUser', JSON.stringify({ email: email, role: role }));

    // Requirement #6: Module-wise redirection using JS
    if (role === 'admin') {
        window.location.href = 'admin.html';
    } else {
        window.location.href = 'user.html';
    }
}

function handleSignup(event) {
    event.preventDefault();
    const email = document.getElementById('signup-email').value;
    const password = document.getElementById('signup-password').value;
    const role = document.getElementById('signup-role').value;

    const users = JSON.parse(localStorage.getItem('users')) || [];
    users.push({ email, password, role });
    
    // Requirement #5: Save to local storage
    localStorage.setItem('users', JSON.stringify(users));
    alert('Signup successful! Please log in.');
    toggleAuthForm();
}

function logOut() {
    localStorage.removeItem('currentUser');
    window.location.href = 'index.html';
}
