# **The CrowdFunding Contract - Planning and Design**

● The Admin will start a campaign for CrowdFunding with a specific monetary goal and deadline.

● Contributors will contribute to that project by sending ETH.

● The admin has to create a Spending Request to spend money for the campaign.

● Once the spending request was created, the Contributors can start voting for that specific Spending Request.

● If more than 50% of the total contributors voted for that request, then the admin would have the permission to spend the amount specified in the spending request. 

● The power is moved from the campaign’s admin to those that donated money.

● The contributors can request a refund if the monetary goal was not reached within the deadline.


# **Solidity Events**

● Each Ethereum transaction has attached to it a receipt which contains zero or more log entries. 

● They are called events in Solidity and Web3, and logs in EVM and Yellow Pages.

● Events allow JavaScript callback functions that listen for them in the user interface to update the interface accordingly.

● Generated events are not accessible from within contracts, not even from the one which has created and emitted them. They can only be accessed by external actors such as JS.

● Events are inheritable members of contracts so if you declare an event in an interface or a base contract you don’t need to declare it in the derived contracts. You just emit it!

● An Event is declared using the event keyword and by convention its name starts with an uppercase letter.

// declare an Event

event Transfer(address _to, uint _value);

● Events are emitted inside setter functions using emit followed by the name of the event.

// emit an Event

emit Transfer(_to, msg.value);

