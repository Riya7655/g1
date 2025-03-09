<html>
<head><title>Ticket Management</title></head>
<body>
    <input id="ticketInput" placeholder="Enter ticket">
    <button onclick="addTicket()">Add</button>
   
    <script>
        function addTicket() {
            let input = document.getElementById("ticketInput");
            if (!input.value.trim()) return;
            let div = document.createElement("div");
            div.innerHTML = `<p>${input.value}</p> <button onclick="this.parentElement.remove()">Delete</button>`;
            document.getElementById("ticketList").appendChild(div);
            input.value = "";
        }
    </script>
</body>
</html>
