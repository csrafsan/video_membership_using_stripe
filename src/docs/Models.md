Model Architecture planning

Membership 
    -slug
    -type(free, pro, enterprise)
    -price
    -stripe plan id

UserMembership
    -user   (foreignkey to default user)
    -stripe customer id
    -membership type    (foreignkey to membership)

Subscription
    -user membership        (foreignkey to Usermembership)
    -stripe subscription id
    -active

Course  
    -slug
    -title
    -allowed memberships(foreignkey to membership)
Lession
    -slug
    -title
    -course (foreignkey to course)
    -position
    -video
    -thumbnail