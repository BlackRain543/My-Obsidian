硬件描述语言
Very-High-Speed Integrated Circuit Hardware DescriptionLanguage

##### 描述性语言

80年代后期

美国国防部

优点：
* 行为描述
* 仿真模拟
* 大规模设计
* 门级网表
* 独立性

#### 4:1 multiplexer
```
library IEEE;
use IEEE.STD_LOGIC_1164.all;
entity mux_4to1 is

 port(
     A,B,C,D : in STD_LOGIC;
     S0,S1: in STD_LOGIC;
     Z: out STD_LOGIC
  );

end mux_4to1;

architecture bhv of mux_4to1 is
begin
	process (A,B,C,D,S0,S1) is
	begin
	  if (S0='0' and S1= '0') then
	      Z<=A;
	  elsif (S0='1' and S1= '0') then
	      Z<=B;
	  elsif (S0='0' and S1= '1') then
	      Z<=C;
	  else
	      Z<=D;
	  end if;
	end process;
end bhv;
```

##### 16-bit D-register with Asynchronous Reset
```
ibrary IEEE;  
use IEEE.std_logic_1164.all;

entity reg16 is  
port( 
	D : in STD_LOGIC_VECTOR(15 downto 0);  
	Q : out STD_LOGIC_VECTOR(15 downto 0);  
	reset,clk,load_en : in STD_LOGIC
);  
end reg16;  
      
architecture behavioural of reg16 is  
signal temp_Q : STD_LOGIC_VECTOR(15 downto 0);  
begin
	process(reset,clk)  
	begin
		if (reset='1') then  
		    temp_Q<="0000 0000 0000 0000";  
		elseif (rising_edge(clk)) then  
		    if (load_en='1') then  
		        temp_Q<=D;     
		    end if;  
		end if;   
		Q <= temp_Q; 
	end process;
end behavioural;
```

