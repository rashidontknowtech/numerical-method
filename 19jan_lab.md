close all
clear all
x=[1,2,3,4,5,6,7];
y=[2,5,4,1,7,8,0];
plot(x,y,'o',MarkerFaceColor='r');

xvec=1:0.01:9;
m=1;
c=0.5;
for m=1:10:100
    for c=-10:2:10
        yvec=m*xvec+c;
      
hold on
plot(xvec,yvec)

ysyn=m*x+c;
plot(x,ysyn,'o',MarkerFaceColor='b');

err_l1=abs(y-ysyn);

    end
end

for m2=1:10:100
    for c2=-10:2:10
        yvec=m2*xvec+c2;
hold on
plot(xvec,yvec);

ysyn2=m2*x+c2;
plot(x,ysyn2,'+',MarkerFaceColor='g')

err_l2=(y-ysyn2).^2;

    end
end

%write code to find the best fit line for l1 and l2
