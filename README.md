oGlow 1.12   
  
Several of the modules use "hooksecurefunc" which wasn't implemented TBC, so these will not work without changes.  
  
  
bags.lua uses it like this -  
  
local self
hooksecurefunc("ContainerFrame_OnShow", function()  
	self = this  
	if(ContainerFrame1.bagsShown > 0) then  
		frame:RegisterEvent"BAG_UPDATE"  
		up[self] = true  
		frame:Show()  
	end  
end)  
