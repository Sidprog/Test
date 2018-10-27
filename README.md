# Test

Thsi my prog

procedure bubbleSort( list : array of items )

   loop = list.count;
   
   for i = 0 to loop-1 do:
      swapped = false
		
      for j = 0 to loop-1 do:
      
            
         if list[j] > list[j+1] then
            
            swap( list[j], list[j+1] )		 
            swapped = true
         end if
         
      end for
      
      
      
      
      if(not swapped) then
         break
      end if
      
   end for
   
end procedure return list
