SetPreventTransmit improvements.

Fully backwards compatible


To use...

( Preventing transmit )
ent:AddPreventTransmitReason( player, "myUniqueReason" )

( un-Preventing transmit )
ent:RemovePreventTransmitReason( player, "myUniqueReason" )


Extra util funcs

( all reasons check, also returns reasons tbl )
bool isPrevented, tbl allReasons = ent:GetPreventTransmit( ply )

( single reason check )
bool hasReason = ent:HasPreventTransmitReason( ply, "myUniqueReason" )


Handles backwards compatibility by just adding/removing a "generic" reason when SetPreventTransmit is called
