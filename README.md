# particle-forces
Forces acting on a particle

clear;
clc;
function [Fx,Fy]=motion(x,y,m,t)
vx=diff(x)./diff(t);
vx=[vx(1),vx];
vy=diff(y)./diff(t);
vy=[vy(1),vy];
ax=diff(vx)./diff(t);
ay=diff(vy)./diff(t);
Fx=m*ax;
Fy=m*ay;
Fx=[Fx(1),Fx];
Fy=[Fy(1),Fy];
plot(t,Fx);
plot(t,Fy)
end
