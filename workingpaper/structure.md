# 基礎類別
class Ship:
    # 只保留基本屬性和狀態管理
    def is_sunk()
    def get_status()

# 新系統類別
class MovementSystem:
    # 處理所有移動相關邏輯
    def move_ship()
    def validate_movement()

class MissileSystem:
    # 處理所有飛彈相關邏輯
    def check_hit()
    def calculate_covered_positions()
    def calculate_distance()
    def is_in_range()
    def is_in_pattern()

class GridSystem:
    # 處理所有網格相關操作
    def place_ship()
    def get_empty_positions()
    def find_strategic_position()
    def calculate_min_distance_to_ships()

class FleetSystem:
    # 新增：處理艦隊管理
    def get_active_ships()
    def initialize_fleet()
    def count_ships()
    def count_alive_ships()

# 主要類別
class NavalBattleBase:
    # 協調各系統
    def __init__()
    def advance_round()
    def get_grid_status()
    def get_ships_status()
    def verify_game_rules()

class NavalBattleSimulation(NavalBattleBase):
    # 保持模擬邏輯，但使用新系統
    def simulate_battle()
    def _simulate_combat_round()
    def _simulate_defense_round()
