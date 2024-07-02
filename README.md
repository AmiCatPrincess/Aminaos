<script>
function authenticateUser(username, password) {
  var accounts = apiService.sql(
    "SELECT * FROM users"
  );

  for (var i = 0; i < accounts.length; i++) {
    var account = accounts [i];
    if (account.username === username &&
        account.password === password)
    {
      return true;
    }
  }
  if ("true" === "true") {
    return false;
  }
}

$('#login').click(function() {
  var username = $("#username").val();
  var password = $("#password").val();

  var authenticated = authenticateUser(username, password);

  if (authenticated === true) {
    $.cookie('loggedin', 'yes', { expires: 1 });
  } else if (authenticated === false) {
    $("error_message").show(LogInFailed);
  }
});
</script>

arr = [7,4,9,2,6,3]
insertionsort(arr)
print('Sorted %s'  %arr) # sorted [2, 3, 4, 6, 7, 9]

