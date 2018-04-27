# ROC

install.packages('pROC')  #下载pROC包

library(pROC) #调用pROC包

#直接画

plot.roc(数据列 ~ 两个分组列, data) 

auc.roc(数据~分组, data) #直接计算auc

#间接画

roc1 <- roc(数据列 ~ 两个分组列, data)

plot(roc1,print.auc=T, auc.polygon=T, grid=c(0.1, 0.2), grid.col=c("green","red"), max.auc.polygon=T, auc.polygon.col="skyblue",print.thres=T)
