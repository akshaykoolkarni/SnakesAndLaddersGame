$(document).ready(function(){
     var flag = true
     var result1 = 0, result2 = 0;
     //starting modals
     $("#closeModal").click(function(){
                 $('#ruleModal').modal({backdrop: 'static', keyboard: false})
                 $("#ruleModal").modal('show');
                     });
     $("#random-100").load(function(){
                      $('#winModal').modal({backdrop: 'static', keyboard: false})
                      $("#winModal").modal('show');
                          });
     $(window).load(function(){
                 $('#myModal').modal({backdrop: 'static', keyboard: false})
                 $('#myModal').modal('show');
             });
     $(document).on('click','#startGame',function(){
                 var player_1 = $('#p1').val();
                 var player_2 = $('#p2').val();
                 $("#player1").html(player_1);
                 $("#player2").html(player_2);
                 if($('#p1').val() == '')
                 {
                    $("#error1").show();
                 }
                 else if($('#p2').val() == '')
                 {
                    $("#error2").show();
                 }
                 else
                 {
                    $("#error1").css("display","none");
                    $("#error2").css("display","none");
                 }

              });
      // at initial players state
      $(".player1").html(result1);
      $(".player2").html(result2);
     // main operation starts here
     $(".dice").click(function(){
        var min = 1;
        var max = 6;
        //formula of random generating by system is:
        var random = Math.floor(Math.random() * (max - min + 1)) + min;
        $('.score').html(random);
        if(flag)
        {
            $("#random-"+result1).css("background","");
            result1  = result1 + random;
            $("#point2").hide();
            $("#point1").show();
             //limiting code to player1 not to go out of 100
             if(result1 > 100)
                 {
                    result1 = result1 - random;
                 }
             else if(result1 == 100)
                 {
                    $(".player1").html(result1);
                        $('#winModal').modal({backdrop: 'static', keyboard: false})
                        $("#winModal").modal('show');
                        $(document).on('click','#random-100',function(){
                            $("#player1").html(player_1);
                        });
                 }
             else if(result1 == 38)
                {
                    result1 = result1 -12;
                }
             else if(result1 == 79)
                {
                    result1 = result1 -60;
                }
             else if(result1 == 89)
                {
                    result1 = result1 - 60;
                }
             else if(result1 == 96)
                {
                    result1 = result1 - 8;
                }
             else if(result1 == 21)
                {
                    result1 = result1 +60;
                }
             else if(result1 == 5)
                {

                    result1 = result1 + 51;
                }
             else if(result1 == 31)
                {
                    result1 = result1 + 59;
                }
             $(".player1").html(result1);
            $("#random-"+result1).css("background-color","red");
            //you can put console to check the results
            flag = false
            }
        else{
            $("#random-"+result2).css("background-color","");
            result2  = result2 + random;
            $("#point2").show();
            $("#point1").hide();
            //limiting code to player2 not to go out of 100
             if(result2 > 100)
                 {
                    result2 = result2 - random;
                 }
             else if(result2 == 100)
                 {
                 $(".player2").html(result2);
                        $('#winModal').modal({backdrop: 'static', keyboard: false})
                        $("#winModal").modal('show');
                        $(document).on('click','#random-100',function(){
                            $("#player2").html(player_2);
                                });
                 }
             else if(result2 == 38)
                 {
                    result2 = result2 -12;
                 }
             else if(result2 == 79)
                {
                    result2 = result2 -60;
                }
             else if(result2 == 89)
                {
                    result2 = result2 -60;
                }
             else if(result2 == 96)
                {
                    result2 = result2 -8;
                }
             else if(result2 == 21)
                {
                    result2 = result2 +60;
                }
             else if(result2 == 5)
                {
                    result2 = result2 + 51;
                }
             else if(result2 == 31)
                {
                    result2 = result2 + 59;
                }
                $(".player2").html(result2);
            $("#random-"+result2).css("background-color", "green");
            flag = true;
        }
    });
});
