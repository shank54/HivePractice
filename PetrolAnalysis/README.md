#### Question1:
Total amount of petrol sold by each distributor
#### Command:
select dist_name, sum(vol_out) from petrol group by dist_name;

#### Question2:
Top 10 sellers along with their id, amount, volume.
#### Command:
select dist_id, vol_out from petrol order by vol_out desc limit 10;

#### Question3:
Top 10 least sellers along with their id, volume_out.
#### Command:
select dist_id, vol_out from petrol order by vol_out limit 10;

#### Question4:
All the distributors having volume difference less than 500 with their name, year, diff.
#### Command:
select dist_name, year, vol_in-vol_out as vol_diff from petrol where vol_in-vol_out<500;
