Framework for SetPreventTransmit to be used by multiple projects without conflicting.
- Works by creating lists of "reasons" for one entity to not be transmitted to a player
- If the list has more than one member, no transmit.


To use...
- ent:AddPreventTransmitReason( player, "myUniqueReason" )
    - Prevents transmit
- ent:RemovePreventTransmitReason( player, "myUniqueReason" )
    - Stops preventing transmit
- ent:SetPreventTransmitReason( player, state, "myUniqueReason" )
    - drop-in replacement for GetPreventTransmit


Extra util funcs

- bool isPrevented, tbl allReasons = ent:GetPreventTransmit( ply )
    - all reasons check, also returns "reasons" tbl
- bool hasReason = ent:HasPreventTransmitReason( ply, "myUniqueReason" )
    - single reason check


Handles backwards compatibility by just adding/removing a "generic" reason when SetPreventTransmit is called
