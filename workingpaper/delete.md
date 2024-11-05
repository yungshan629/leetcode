Cell 1:
class Ship:
    # 刪除這些方法，移至其他系統
    def move(self)                     # 移至 MovementSystem
    def appear_on_grid(self)           # 移至 GridSystem

class NavalBattleBase:
    # 刪除這些方法，移至其他系統
    def _place_ship_at_position()      # 移至 GridSystem
    def _find_strategic_position()     # 移至 GridSystem
    def _calculate_min_distance_to_ships()  # 移至 GridSystem
    def _get_all_empty_positions()     # 移至 GridSystem
    
    # 飛彈相關方法全部移至 MissileSystem
    def _check_missile_hit()           # 移至 MissileSystem
    def _is_in_missile_range()         # 移至 MissileSystem
    def _is_in_attack_pattern()        # 移至 MissileSystem
    def _calculate_covered_positions()  # 移至 MissileSystem
    def visualize_attack_range()       # 移至 MissileSystem

    Cell 2:
    class MissileSelectionMatrix:
    # 刪除重複定義的部分
    @classmethod
    def calculate_ammo_score()         # 保留第一個定義，刪除重複的
    @classmethod 
    def calculate_range_score()        # 保留第一個定義，刪除重複的

    Cell 3:
    lass NavalBattleSimulation:
    # 這些方法不需要刪除，但需要修改為使用新系統
    def _execute_move()                # 改用 MovementSystem
    def _simulate_combat_round()       # 改用新系統
    def _simulate_defense_round()      # 改用新系統
    def _attack_with_all_ships()       # 改用新系統
    
    # 這些輔助方法移至對應系統
    def _calculate_distance()          # 移至 MissileSystem
    def _get_active_ships()           # 移至新的 FleetSystem
