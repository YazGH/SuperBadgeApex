# SuperBadgeApex
Codigo realizado para el SuperBadgeApex


Asi se ejecuta el trigger desde la ventana anonima:

Map<Id,Case> caseMap  = new Map<Id,Case>([Select id 
                                          from Case 
                                          where Type ='Routine Maintenance' and Status ='New'
                                         ]);
for(Case c: caseMap.values()){
    c.Status = 'Closed';
}

update caseMap.values();
