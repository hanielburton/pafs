# PL/SQL API for Stripe

Credit: Originally forked from Trent Schafer, his blog post was key to getting me started with Stripe integration. You can read about it here:https://apextips.blogspot.com/2016/02/accepting-payments-with-stripe-in-apex_26.html

Since I was building out the rest of the API for myself I thought others might find it useful as well. 

This API is used to charge cards from an APEX application. Basic usage:

```plsql
begin

    stripe_api.set_secret('[secret removed]');
    
    stripe_api.charge_card(
        p_amount => 300
      , p_source => '[token_removed]'
      , p_description => '..'
    );

end;
```
