
## Updated 7/11/2016

x<- read.csv(file.choose())
library(metafor)

#Grey boxes underneath pollutant categories
# par(mar=c(5.1, 4.1, 1, 2))
# plot(c(-25,35), c(0,40),  type = "n", xlab = "", ylab = "", axes=F)


par(mar=c(5.1, 4.1, 1, 2))

par(font=1)
forest(x$ne[which(x$pollutant=="Ambient PM")], 
       ci.lb=x$ne_lb[which(x$pollutant=="Ambient PM")], ci.ub=x$ne_ub[which(x$pollutant=="Ambient PM")],                  
       xlab='', at=c(-5, 0, 5, 10, 15, 20), slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(35), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$ne[which(x$pollutant=="Individual PM")], 
       ci.lb=x$ne_lb[which(x$pollutant=="Individual PM")], ci.ub=x$ne_ub[which(x$pollutant=="Individual PM")],                  
       xlab='', xaxt='n', xaxt='n',slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(33), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$ne[which(x$pollutant=="NOx")], 
       ci.lb=x$ne_lb[which(x$pollutant=="NOx")], ci.ub=x$ne_ub[which(x$pollutant=="NOx")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(31), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))
par(new=T)
forest(x$ne[which(x$pollutant=="NO2")], 
       ci.lb=x$ne_lb[which(x$pollutant=="NO2")], ci.ub=x$ne_ub[which(x$pollutant=="NO2")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(29), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$ne[which(x$pollutant=="Black Carbon")], 
       ci.lb=x$ne_lb[which(x$pollutant=="Black Carbon")], ci.ub=x$ne_ub[which(x$pollutant=="Black Carbon")],                  
       xlab='% Difference in Catecholamines', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(27), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))


rect(-80, 36, 40, 38, col="gray85", border="gray85")
rect(-80, 23, 40, 25, col="gray85", border="gray85")
rect(-80, 10, 40, 12, col="gray85", border="gray85")


par(font=2)
#Outcome titles
text(-24, 37, labels="Norepinephrine", pos=4)
text(-24, 24, labels="Epinephrine", pos=4)
text(-24, 11, labels="Dopamine", pos=4)

par(font=1)
text(35, 37, labels="% Difference (95% CI)", cex=0.9, pos=2)
text(35, 24, labels="% Difference (95% CI)", cex=0.9, pos=2)
text(35, 11, labels="% Difference (95% CI)", cex=0.9, pos=2)

par(font=1)
text(-23, 35, labels=expression("Ambient PM"[2.5]), cex=0.95, pos=4)
text(-23, 33, labels=expression("Individual PM"[2.5]), cex=0.95, pos=4)
text(-23, 31, labels=expression("NO"[x]), cex=0.95, pos=4)
text(-23, 29, labels=expression("NO"[2]), cex=0.95, pos=4)
text(-23, 27, labels="Black Carbon", cex=0.95, pos=4)

text(-23, 22, labels=expression("Ambient PM"[2.5]), cex=0.95, pos=4)
text(-23, 20, labels=expression("Individual PM"[2.5]), cex=0.95, pos=4)
text(-23, 18, labels=expression("NO"[x]), cex=0.95, pos=4)
text(-23, 16, labels=expression("NO"[2]), cex=0.95, pos=4)
text(-23, 14, labels="Black Carbon", cex=0.95, pos=4)

text(-23, 9, labels=expression("Ambient PM"[2.5]), cex=0.95, pos=4)
text(-23, 7, labels=expression("Individual PM"[2.5]), cex=0.95, pos=4)
text(-23, 5, labels=expression("NO"[x]), cex=0.95, pos=4)
text(-23, 3, labels=expression("NO"[2]), cex=0.95, pos=4)
text(-23, 1, labels="Black Carbon", cex=0.95, pos=4)
# 
# par(mar=c(5.1, 1, 4.1, 1))
# par(new=T)
# plot(c(-25, 40), c(0, 23),  type = "n", xlab = "", ylab = "", axes=F)
# rect(-50, 20.25, 45, 21.5, col=c("gray85"), border=c("gray85"))
# rect(-50, 9.35, 45, 10.6, col=c("gray85"), border=c("gray85"))



par(font=1)
par(new=T)
forest(x$epi[which(x$pollutant=="Ambient PM")], 
       ci.lb=x$epi_lb[which(x$pollutant=="Ambient PM")], ci.ub=x$epi_ub[which(x$pollutant=="Ambient PM")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(22), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$epi[which(x$pollutant=="Individual PM")], 
       ci.lb=x$epi_lb[which(x$pollutant=="Individual PM")], ci.ub=x$epi_ub[which(x$pollutant=="Individual PM")],                  
       xlab='', xaxt='n', xaxt='n',slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(20), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$epi[which(x$pollutant=="NOx")], 
       ci.lb=x$epi_lb[which(x$pollutant=="NOx")], ci.ub=x$epi_ub[which(x$pollutant=="NOx")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(18), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))
par(new=T)
forest(x$epi[which(x$pollutant=="NO2")], 
       ci.lb=x$epi_lb[which(x$pollutant=="NO2")], ci.ub=x$epi_ub[which(x$pollutant=="NO2")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(16), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$epi[which(x$pollutant=="Black Carbon")], 
       ci.lb=x$epi_lb[which(x$pollutant=="Black Carbon")], ci.ub=x$epi_ub[which(x$pollutant=="Black Carbon")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(14), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))




par(font=1)
par(new=T)
forest(x$da[which(x$pollutant=="Ambient PM")], 
       ci.lb=x$da_lb[which(x$pollutant=="Ambient PM")], ci.ub=x$da_ub[which(x$pollutant=="Ambient PM")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(9), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$da[which(x$pollutant=="Individual PM")], 
       ci.lb=x$da_lb[which(x$pollutant=="Individual PM")], ci.ub=x$da_ub[which(x$pollutant=="Individual PM")],                  
       xlab='', xaxt='n', xaxt='n',slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(7), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$da[which(x$pollutant=="NOx")], 
       ci.lb=x$da_lb[which(x$pollutant=="NOx")], ci.ub=x$da_ub[which(x$pollutant=="NOx")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(5), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))
par(new=T)
forest(x$da[which(x$pollutant=="NO2")], 
       ci.lb=x$da_lb[which(x$pollutant=="NO2")], ci.ub=x$da_ub[which(x$pollutant=="NO2")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(3), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))

par(new=T)
forest(x$da[which(x$pollutant=="Black Carbon")], 
       ci.lb=x$da_lb[which(x$pollutant=="Black Carbon")], ci.ub=x$da_ub[which(x$pollutant=="Black Carbon")],                  
       xlab='', xaxt='n', slab=c(NA), digits=c(0), annotate=F, psize=1,  refline=0, 
       rows=c(1), ylim=c(0,40), xlim=c(-25,35), alim=c(-5,20))


text(21,35,labels=paste(format(round(x$ne[which(x$pollutant=="Ambient PM")],1),nsmall=1)," (",
                       format(round(x$ne_lb[which(x$pollutant=="Ambient PM")],1),nsmall=1),", ",
                       format(round(x$ne_ub[which(x$pollutant=="Ambient PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,33,labels=paste(format(round(x$ne[which(x$pollutant=="Individual PM")],1),nsmall=1)," (",
                       format(round(x$ne_lb[which(x$pollutant=="Individual PM")],1),nsmall=1),", ",
                       format(round(x$ne_ub[which(x$pollutant=="Individual PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,31,labels=paste(format(round(x$ne[which(x$pollutant=="NOx")],1),nsmall=1)," (",
                       format(round(x$ne_lb[which(x$pollutant=="NOx")],1),nsmall=1),", ",
                       format(round(x$ne_ub[which(x$pollutant=="NOx")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,29,labels=paste(format(round(x$ne[which(x$pollutant=="NO2")],1),nsmall=1)," (",
                          format(round(x$ne_lb[which(x$pollutant=="NO2")],1),nsmall=1),", ",
                          format(round(x$ne_ub[which(x$pollutant=="NO2")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,27,labels=paste(format(round(x$ne[which(x$pollutant=="Black Carbon")],1),nsmall=1)," (",
                          format(round(x$ne_lb[which(x$pollutant=="Black Carbon")],1),nsmall=1),", ",
                          format(round(x$ne_ub[which(x$pollutant=="Black Carbon")],1),nsmall=1),")",sep=""),cex=.8, pos=4)


text(21,22,labels=paste(format(round(x$epi[which(x$pollutant=="Ambient PM")],1),nsmall=1)," (",
                       format(round(x$epi_lb[which(x$pollutant=="Ambient PM")],1),nsmall=1),", ",
                       format(round(x$epi_ub[which(x$pollutant=="Ambient PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,20,labels=paste(format(round(x$epi[which(x$pollutant=="Individual PM")],1),nsmall=1)," (",
                       format(round(x$epi_lb[which(x$pollutant=="Individual PM")],1),nsmall=1),", ",
                       format(round(x$epi_ub[which(x$pollutant=="Individual PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,18,labels=paste(format(round(x$epi[which(x$pollutant=="NOx")],1),nsmall=1)," (",
                       format(round(x$epi_lb[which(x$pollutant=="NOx")],1),nsmall=1),", ",
                       format(round(x$epi_ub[which(x$pollutant=="NOx")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,16,labels=paste(format(round(x$epi[which(x$pollutant=="NO2")],1),nsmall=1)," (",
                          format(round(x$epi_lb[which(x$pollutant=="NO2")],1),nsmall=1),", ",
                          format(round(x$epi_ub[which(x$pollutant=="NO2")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,14,labels=paste(format(round(x$epi[which(x$pollutant=="Black Carbon")],1),nsmall=1)," (",
                          format(round(x$epi_lb[which(x$pollutant=="Black Carbon")],1),nsmall=1),", ",
                          format(round(x$epi_ub[which(x$pollutant=="Black Carbon")],1),nsmall=1),")",sep=""),cex=.8, pos=4)


text(21,9,labels=paste(format(round(x$da[which(x$pollutant=="Ambient PM")],1),nsmall=1)," (",
                       format(round(x$da_lb[which(x$pollutant=="Ambient PM")],1),nsmall=1),", ",
                       format(round(x$da_ub[which(x$pollutant=="Ambient PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,7,labels=paste(format(round(x$da[which(x$pollutant=="Individual PM")],1),nsmall=1)," (",
                       format(round(x$da_lb[which(x$pollutant=="Individual PM")],1),nsmall=1),", ",
                       format(round(x$da_ub[which(x$pollutant=="Individual PM")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(21,5,labels=paste(format(round(x$da[which(x$pollutant=="NOx")],1),nsmall=1)," (",
                       format(round(x$da_lb[which(x$pollutant=="NOx")],1),nsmall=1),", ",
                       format(round(x$da_ub[which(x$pollutant=="NOx")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(20.75,3,labels=paste(format(round(x$da[which(x$pollutant=="NO2")],1),nsmall=1)," (",
                       format(round(x$da_lb[which(x$pollutant=="NO2")],1),nsmall=1),", ",
                       format(round(x$da_ub[which(x$pollutant=="NO2")],1),nsmall=1),")",sep=""),cex=.8, pos=4)

text(20.75,1,labels=paste(format(round(x$da[which(x$pollutant=="Black Carbon")],1),nsmall=1)," (",
                         format(round(x$da_lb[which(x$pollutant=="Black Carbon")],1),nsmall=1),", ",
                         format(round(x$da_ub[which(x$pollutant=="Black Carbon")],1),nsmall=1),")",sep=""),cex=.8, pos=4)
# 
# text(0.35,6,labels=paste(format(round(no2_mi[3],2),nsmall=2)," (",no2_mi_lb[3],",",format(round(no2_mi_ub[3],2),nsmall=2),")",sep=""),cex=.75, pos=2)
# text(0.35,5,labels=paste(no2_mi[4]," (",no2_mi_lb[4],",",no2_mi_ub[4],")",sep=""),cex=.75, pos=2)



