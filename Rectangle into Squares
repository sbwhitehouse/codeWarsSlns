#include <iostream>
#include <vector>

class SqInRect
{
  public:
  static std::vector<int> sqInRect(int lng, int wdth) {
    //Return nothing if lng == wdth
    std::vector<int> squares = {};
    if(lng == wdth) return {};
    //Variables to track the necessary attributes of the rectangle
    int area = lng * wdth;
    int long_side = std::max(lng,wdth);
    int prev_long_side = long_side;
    int short_side = std::min(lng,wdth);
    for(int i = short_side; i > 0; i = short_side) {
        if(area - (i * i) >= 0) {
            //Track the long side 1 square back
            prev_long_side = long_side;
            //Only change the short_side if it is actually decreasing
            if(short_side >= long_side - short_side) {
               short_side = long_side - short_side;
            }
            long_side = prev_long_side - short_side;
            squares.push_back(i);
            area -= (i * i);
        }
        else {
            short_side = long_side - short_side;
        }
    }

    return squares;
  }
  
};
