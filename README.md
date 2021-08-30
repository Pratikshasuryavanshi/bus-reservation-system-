1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
void a::reservation()
{
int bus_seat;
char no[5];
top:
cout&lt;&lt;"Bus Number: ";
cin&gt;&gt;no;
int y;
for(y=0;y&lt;=t;y++)
{
if(strcmp(bus[y].bus_number, no)==0) break;
}
while(y&lt;=t)
{
cout&lt;&lt;"\nSeat Number: "; cin&gt;&gt;bus_seat; if(bus_seat&gt;32) { cout&lt;&lt;"\nThere are only 32 Seats Available in this Bus."; } else { if (strcmp(bus[y].bus_seat[bus_seat/4][(bus_seat%4)-1], "Empty")==0) { cout&lt;&lt;"Enter Passenger's Name: "; cin&gt;&gt;bus[y].bus_seat[bus_seat/4][(bus_seat%4)-1]; break; } else cout&lt;&lt;"The Seat Number. is Already Reserved.\n"; } } if(y&gt;t) { cout&lt;&lt;"Enter Correct Bus Number.\n"; goto top; }
}
